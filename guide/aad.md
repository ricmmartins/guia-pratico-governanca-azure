## Azure Active Directory

Para começarmos a entender mais detalhadamente sobre os principais serviços relacionados com a Governança do Azure, é importante começarmos falando sobre a relação do Azure Active Directory (AAD) com as assinaturas. Não será abordado todos os detalhes sobre ele aqui, uma vez que este não é o propósito deste documeto. No entanto veremos aqui o básico do seu funcionamento e a diferença entre o Azure Active Directory (AAD) e o Active Directory (AD).

O AAD é o serviço de gerenciamento de identidade e acessos baseado na nuvem que irá permitir que você conceda acesso para usuários, grupos e aplicações nos serviços do Azure assim como também permite que você defina como eles irão utilizar os recursos do Azure através das funções que você irá atribuir à eles. Desta forma, ele fará o papel de gerenciar a autorização e autenticação para os serviços do Azure.


Ao criar uma assinatura do Azure, um **tenant** do AAD é automaticamente criado. O **tenant** nada mais é que a representação do domínio da sua empresa dentro do Azure Active Directory. Note que por padrão você sempre irá ganhar um **nome.onmicrosoft.com** que depois você pode customizar para **seudominio.com**. 

Dentro do seu **tenant**  do AAD você terá o seu diretório do AAD que é onde você irá criar seus usuários e grupos. Note que você também pode fazer um sincronismo dos seus usuários já existentes no seu Active Directory existente para o Azure Active Directory através do Azure AD Connect, mas este assunto não será abordado aqui. 

Então basicamente a principal diferença do Active Directory para o Azure Active Directory é que o AAD tem por objetivo trabalhar exclusivamente a **autorização e autenticação dos seus usuários, grupos  e aplicações nos serviços do Azure**. Em contrapartida o Active Directory faz a autorização e autenticação no ambiente on-premises além de muitas outras tarefas como gerenciamento de GPOS e servidores Windows. [Neste link](https://docs.microsoft.com/pt-br/azure/active-directory/fundamentals/active-directory-compare-azure-ad-to-ad) existe uma comparação mais ampla entre eles.


### Pro tip!

✔️ [Azure AD Identity Governance](https://docs.microsoft.com/pt-br/azure/active-directory/governance/identity-governance-overview)
<br>
✔️ [Azure AD access reviews](https://docs.microsoft.com/pt-br/azure/active-directory/governance/access-reviews-overview)

---

Anterior| Próximo | 
:----- |:-----
[Arquitetura de governança no Azure](/guide/aad.md)| [Padrões de nomes](/guide/naming.md)
