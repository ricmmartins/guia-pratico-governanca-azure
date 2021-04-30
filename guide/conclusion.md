## Conclusion

### Azure DevOps Governance Generator

Agora que você conhece a importância de adotar a Governança e quais ferramentas o Azure disponibiliza para você implementar, que tal começar a colocá-la em prática?

Ter um conselho contendo todas as informações relacionadas à governança, desde os detalhes de como funciona até os detalhes de como implementá-la, pode ser útil? Além disso, se você pudesse compartilhar este quadro com toda a sua equipe para discutir cada ponto, delegar atividades, criar iterações e acompanhar o andamento de cada tarefa, seria interessante?

Então visite [https://aka.ms/azgovernancereadiness](https://aka.ms/azgovernancereadiness) e descubra como usar o Azure DevOps Generator gratuitamente para começar a implementar a Governança do Azure em sua organização.

![governance-devopsgenerator](../images/governance-devopsgenerator.png)


### Azure Governance Visualizer

O que você acha de ter uma representação gráfica da implementação de sua governança? Deixe-me apresentar uma das minhas ferramentas favoritas: [AzGovViz](https://github.com/JulianHayward/Azure-MG-Sub-Governance-Reporting).

O AzGovViz (visualizador de governança do Azure) é um script do PowerShell que itera por meio de uma hierarquia do management group do tenant do Azure até o nível de assinatura. Ele captura dados dos recursos de governança do Azure mais relevantes, como Políticas , controle de acesso baseado em função do Azure (Azure RBAC) e Blueprints do Azure. A partir dos dados coletados, o visualizador mostra seu mapa de hierarquia, cria um resumo do tenant e constrói percepções de escopo granular sobre seus grupos de gerenciamento e assinaturas.


![azgovviz](https://github.com/JulianHayward/Azure-MG-Sub-Governance-Reporting/blob/master/img/HierarchyMap.png)

---

Anterior |  
:----- 
[Azure Cost Management](/guide/cost-management.md)| 
