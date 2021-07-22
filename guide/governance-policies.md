## Políticas sugeridas para governança

Aqui está uma lista de políticas sugeridas que você pode aplicar em seu ambiente para ajudar em sua abordagem de governança.

### ☑️ Computação
**SKUs de tamanho de máquina virtual permitidos:** Esta política permite que você especifique um conjunto de SKUs de tamanho de máquina virtual que sua organização pode implantar.
|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fcccc23c7-8427-4f53-ad12-b6a63eb452b3)|[Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Compute/VMSkusAllowed_Deny.json)|
|--- |--- |

### ☑️ Geral
**Locais permitidos:** Esta política permite que você restrinja os locais que sua organização pode especificar ao implantar recursos. Use para fazer cumprir seus requisitos de conformidade geográfica. Exclui grupos de recursos, Microsoft.AzureActiveDirectory/b2cDirectories e recursos que usam a região 'global'.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fe56962a6-4747-49cd-b67b-bf8b01975c4c)|[Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/AllowedLocations_Deny.json)|
|--- |--- |

**Locais permitidos para grupos de recursos:** Esta política permite que você restrinja os locais em que sua organização pode criar grupos de recursos. Use para impor seus requisitos de conformidade geográfica.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fe765b5de-1225-4ba3-bd56-1ac6695af988) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/ResourceGroupAllowedLocations_Deny.json)|
|--- |--- |

**Tipos de recursos permitidos:** Esta política permite que você especifique os tipos de recursos que sua organização pode implantar. Apenas os tipos de recursos que suportam 'tags' e 'localização' serão afetados por esta política. Para restringir todos os recursos, duplique esta política e altere o 'modo' para 'Todos'.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fa08ec900-254a-4555-9bf5-e42af04b5c5c) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/AllowedResourceTypes_Deny.json)|
|--- |--- |

**Auditar se a localização do recurso corresponde à localização do grupo de recursos:** Audite se a localização do recurso corresponde à localização do grupo de recursos.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F0a914e76-4921-4c19-b460-a2d36003525a) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/ResourcesInResourceGroupLocation_Audit.json)|
|--- |--- |

**Auditar o uso de regras RBAC personalizadas:** Auditar funções integradas, como 'Proprietário, Contribuidor, Leitor' em vez de funções RBAC personalizadas, que são sujeitas a erros. O uso de funções personalizadas é tratado como uma exceção e requer uma análise rigorosa e modelagem de ameaças.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fa451c1ef-c6ca-483d-87ed-f49761e3ffb5) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/Subscription_AuditCustomRBACRoles_Audit.json)|
|--- |--- |

**As funções customizadas de proprietário de assinatura não devem existir:** Esta política garante que nenhuma função customizada de proprietário de assinatura exista.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F10ee2ea2-fb4d-45b8-a7e9-a2e770044cd9) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/CustomSubscription_OwnerRole_Audit.json)|
|--- |--- |

**Tipos de recursos não permitidos:** Restrinja os tipos de recursos que podem ser implantados em seu ambiente. Limitar os tipos de recursos pode reduzir a complexidade e a superfície de ataque do seu ambiente, ao mesmo tempo que ajuda a gerenciar os custos. Os resultados de conformidade são mostrados apenas para recursos não compatíveis.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F6c112d4e-5bc7-47ae-a041-ea2d9dccd749) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/General/InvalidResourceTypes_Deny.json)|
|--- |--- |

### ☑️ Segurança
✔️ *Observe que se você decidir habilitar as iniciativas internas da Central de Segurança do Azure, fique atento a conflitos sobrepostos. [Veja aqui](https://docs.microsoft.com/en-us/azure/security-center/policy-reference) as definições internas da Política do Azure para a Central de Segurança do Azure*

**No máximo 3 proprietários devem ser designados para sua assinatura:** Recomenda-se designar até 3 proprietários de assinatura para reduzir o potencial de violação por um proprietário comprometido.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F4f11b553-d42e-4e3a-89be-32ca364cad4c) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Security%20Center/ASC_DesignateLessThanXOwners_Audit.json)|
|--- |--- |

**MFA deve ser habilitado em contas com permissões de proprietário em sua assinatura:** Multi-Factor Authentication (MFA) deve ser habilitado para todas as contas de assinatura com permissões de proprietário para evitar uma violação de contas ou recursos.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Faa633080-8b72-40c4-a2d7-d00c03e80bed) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Security%20Center/ASC_EnableMFAForOwnerPermissions_Audit.json)|
|--- |--- |

**As assinaturas devem ter um endereço de e-mail de contato para questões de segurança:** Para garantir que as pessoas relevantes em sua organização sejam notificadas quando houver uma potencial violação de segurança em uma de suas assinaturas, defina um contato de segurança para receber notificações por e-mail da Central de Segurança.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F4f4f78b8-e367-4b10-a341-d9a4ad5cf1c7) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Security%20Center/ASC_Security_contact_email.json)|
|--- |--- |

**Deve haver mais de um proprietário atribuído à sua assinatura:** Recomenda-se designar mais de um proprietário de assinatura para ter redundância de acesso de administrador.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F09024ccc-0c5f-475e-9457-b7c0d9ed487b) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Security%20Center/ASC_DesignateMoreThanOneOwner_Audit.json)|
|--- |--- |


### ☑️ Tags
**Exigir uma tag em grupos de recursos:** Impõe a existência de uma tag em grupos de recursos.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F96670d01-0a4d-4649-9c89-2d3abc0a5025) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupRequireTag_Deny.json)|
|--- |--- |

**Herdar uma tag do grupo de recursos se ausente:** Adiciona a tag especificada com seu valor do grupo de recursos pai quando qualquer recurso sem esta tag é criado ou atualizado. Os recursos existentes podem ser corrigidos acionando uma tarefa de correção. Se a tag existir com um valor diferente, ela não será alterada.

|[Clique aqui para ver no portal do Azure](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Fea3f2387-9b95-492a-a190-fcdc54f7b070) | [Clique aqui para ver o arquivo JSON](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Add_Modify.json)|
|--- |--- |

---

Anterior| Próximo | 
:----- |:-----
[Azure Policy Best Practices](/guide/policy-best-practices.md)| [ARM Templates](/guide/arm.md)
