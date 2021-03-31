---
title: Sondando alterações usando o controle DirSync
description: Active Directory controle de sincronização de diretório (DirSync) é uma extensão de servidor LDAP que permite que um aplicativo pesquise uma partição de diretório para objetos que foram alterados desde um estado anterior.
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- Sondando alterações usando o AD do controle DirSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d105757d39bc25bd10df21ab68c4d1d1202be
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640392"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>Sondando alterações usando o controle DirSync

Active Directory controle de sincronização de diretório (DirSync) é uma extensão de servidor LDAP que permite que um aplicativo pesquise uma partição de diretório para objetos que foram alterados desde um estado anterior.

Use o controle DirSync por meio da ADSI especificando a preferência de pesquisa **\_ \_ DirSync do ADS SEARCHPREF** ao usar o [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Para obter mais informações e um exemplo de código, consulte [código de exemplo usando o ADS \_ SEARCHPREF \_ DirSync](example-code-using-ads-searchpref-dirsync.md). Você também pode executar uma pesquisa DirSync usando a API LDAP. A seguir, a descrição da implementação de ADSI, a maioria das quais também se aplica ao uso do LDAP diretamente, exceto como discutido no final deste tópico.

Ao executar uma pesquisa do DirSync, você passa um elemento de dados específico do provedor (cookie) que identifica o estado do diretório no momento da pesquisa do DirSync anterior. Para a primeira pesquisa, você passa um cookie nulo e a pesquisa retorna todos os objetos que correspondem ao filtro. A pesquisa também retorna um cookie válido. Armazene o cookie no mesmo armazenamento que você está sincronizando com o servidor de Active Directory. Em pesquisas subsequentes, obtenha o cookie do armazenamento e passe-o com a solicitação de pesquisa. Os resultados da pesquisa agora incluem apenas os objetos e atributos que foram alterados desde o estado anterior identificado pelo cookie. A pesquisa também retorna um novo cookie a ser armazenado para a próxima pesquisa.

A tabela a seguir lista os parâmetros de pesquisa que a solicitação de pesquisa do cliente pode especificar.



| Parâmetro          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base da pesquisa | A base de uma pesquisa DirSync deve ser a raiz de uma partição de diretório, que pode ser uma partição de domínio, a partição de configuração ou a partição de esquema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Escopo              | O escopo de uma pesquisa DirSync deve ser **a \_ \_ subárvore de escopo ADS**, ou seja, toda a subárvore da partição. Lembre-se de que, para uma pesquisa de uma partição de domínio, a subárvore inclui os cabeçalhos, mas não o conteúdo, da configuração e das partições de esquema. Para pesquisar alterações em um escopo menor, use a técnica **USNChanged** em vez de DirSync.                                                                                                                                                                                                                                                                                                                                                                                 |
| Filtrar             | Você pode especificar qualquer filtro de pesquisa válido. Para uma pesquisa inicial com um cookie nulo, os resultados incluem todos os objetos que correspondem ao filtro. Para pesquisas subsequentes com um cookie válido, os resultados da pesquisa incluem dados somente para objetos que correspondam ao filtro e foram alterados desde o estado indicado pelo cookie. Para obter mais informações sobre filtros de pesquisa, consulte [criando um filtro de consulta](creating-a-query-filter.md).                                                                                                                                                                                                                                                                                                                |
| Atributos         | Você pode especificar uma lista de atributos a serem retornados quando ocorrer uma alteração. Para cada objeto, os resultados iniciais incluem todos os atributos solicitados definidos no objeto. Os resultados da pesquisa subsequentes incluem apenas os atributos especificados que foram alterados. Os atributos inalterados não são incluídos nos resultados da pesquisa. Na implementação do ADSI, os resultados da pesquisa sempre incluem o **objectGUID** e o **InstanceType** de cada objeto. Além disso, a lista de atributos especificada atua como um filtro adicional: os resultados da pesquisa inicial incluem apenas objetos que tenham pelo menos um dos atributos especificados definidos; as pesquisas subsequentes incluem apenas objetos dos quais um ou mais atributos foram alterados (valores adicionados ou excluídos). |



 

Além disso, lembre-se de que:

-   Para pesquisas incrementais, a prática recomendada é associar-se ao mesmo controlador de domínio (DC) usado na pesquisa anterior, ou seja, o DC que gerou o cookie. Se o mesmo DC não estiver disponível, aguarde até que ele seja ou associe a um novo DC e execute uma sincronização completa. Armazene o nome DNS do controlador de domínio no armazenamento secundário com o cookie.

    Você pode passar um cookie gerado por um DC para um controlador de domínio diferente que hospeda uma réplica da mesma partição de diretório. Não há nenhuma chance de um cliente perder as alterações usando um cookie de um DC em outro DC. No entanto, é possível que os resultados da pesquisa do novo DC possam incluir alterações relatadas pelo controlador de domínio antigo; em alguns casos, o novo DC pode retornar todos os objetos e atributos, assim como ocorre com uma sincronização completa. O cliente deve apenas tornar seu banco de dados consistente com os resultados de pesquisa relatados para qualquer chamada DirSync fornecida, ou seja, tratar todos os resultados incrementais como se fossem o estado mais recente. Não importa se você viu a alteração antes ou se está até voltando para um estado anterior porque as sincronizações incrementais repetidas convergirão na consistência.

-   Quando um objeto é renomeado ou movido, seus objetos filho, se houver, não são incluídos nos resultados da pesquisa, embora os nomes distintos dos objetos filho tenham mudado. Da mesma forma, quando uma ACE herdável é modificada em um descritor de segurança de objeto, os objetos filho do objeto não são incluídos nos resultados da pesquisa, mesmo que os descritores de segurança dos objetos filho tenham mudado.
-   Use o atributo **objectGUID** para identificar os objetos rastreados. O **objectGUID** de cada objeto permanece inalterado, independentemente de onde o objeto é movido dentro da floresta.
-   Lembre-se de que os resultados da pesquisa de uma pesquisa do DirSync indicam o estado dos objetos em uma réplica da partição de diretório no momento da pesquisa. Isso significa que as alterações feitas em outros DCs não serão incluídas se não tiverem sido replicadas no controlador de domínio de destino. Isso também significa que os atributos de um objeto podem ter mudado várias vezes desde a pesquisa do DirSync anterior, mas a pesquisa mostrará apenas o estado final, não a sequência de alterações.
-   Na implementação do ADSI, o aplicativo deve tratar o cookie como opaco e não fazer suposições sobre sua organização ou valor interno.
-   Lembre-se de que o cliente armazena o cookie, o comprimento do cookie e o nome DNS do controlador de domínio no mesmo armazenamento que contém os dados do objeto sincronizado. Isso garante que o cookie e outros parâmetros permaneçam sincronizados com os dados do objeto se o armazenamento for restaurado de um backup.
-   Para recuperar o atributo [**parentGUID**](/windows/desktop/ADSchema/a-parentguid) , que é construído para o controle DirSync, também é necessário solicitar o atributo [**Name**](/windows/desktop/ADSchema/a-name) .

Para usar o controle DirSync, o chamador deve ter o direito "diretório obter alterações" atribuído na raiz da partição que está sendo monitorada. Por padrão, esse direito é atribuído às contas de administrador e LocalSystem em controladores de domínio. O chamador também deve ter o direito de acesso de controle estendido [**DS-Replication-Get-Changes**](/windows/desktop/ADSchema/r-ds-replication-get-changes) . Para obter mais informações sobre como implementar um mecanismo de controle de alterações para aplicativos que devem ser executados em uma conta que não tem esse direito, consulte [sondando alterações usando USNChanged](polling-for-changes-using-usnchanged.md). Para obter mais informações sobre privilégios, consulte [privilégios](/windows/desktop/SecAuthZ/privileges).

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>Recuperando objetos excluídos com uma pesquisa DirSync

Os resultados da pesquisa do **\_ SEARCHPREF \_ DirSync de anúncios** incluem automaticamente os objetos excluídos (marcas para exclusão) que correspondem ao filtro de pesquisa especificado. No entanto, um filtro de pesquisa que corresponderá a um objeto quando ele estiver ativo pode não corresponder ao objeto depois que ele for excluído. Isso ocorre porque as marcas para exclusão retêm apenas um subconjunto dos atributos presentes no objeto original. Por exemplo, normalmente você usaria o filtro a seguir para objetos de usuário.


```C++
(&(objectClass=user)(objectCategory=person))
```



O atributo **objectCategory** é removido quando um objeto é excluído, portanto, o filtro acima não corresponderia a quaisquer objetos de marca para exclusão. Por outro lado, o atributo **objectClass** é retido em objetos de marca para exclusão, de modo que um filtro de "(objectClass = user)" corresponderá a objetos de usuário excluídos.

A lista de atributos que você especifica com uma pesquisa DirSync também atua como um filtro; os resultados da pesquisa incluem apenas objetos nos quais um ou mais dos atributos especificados foram alterados desde a pesquisa do DirSync anterior. Se a lista de atributos não incluir atributos que são retidos em marcas de exclusão, os resultados da pesquisa não incluirão marcas de exclusão. Para lidar com isso, solicite todos os atributos especificando uma lista de atributos nulos; ou você pode solicitar o atributo **IsDeleted** , definido como **true** em todas as marcas para exclusão. Os atributos de marca para exclusão têm o bit 0x8 definido no atributo **searchFlags** da definição **attributeSchema** .

Para obter mais informações, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).

## <a name="ldap-implementation-of-the-dirsync-control"></a>Implementação de LDAP do controle DirSync

Você também pode executar uma pesquisa DirSync usando a API LDAP com o controle [ \_ \_ \_ OID do servidor LDAP](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) . Se você usar a API LDAP, especifique também o [ \_ \_ \_ \_ OID DN estendido do servidor LDAP](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) e o [ \_ servidor LDAP mostrar controles \_ \_ \_ OID excluídos](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . O \_ \_ controle OID do DN estendido do servidor LDAP \_ \_ faz com que uma pesquisa LDAP retorne uma forma estendida do nome distinto que inclui o **objectGUID** e o **objectSid** para objetos de entidade de segurança, como usuários, grupos e computadores. O \_ servidor LDAP \_ Mostrar \_ \_ controle de OID excluído faz com que os resultados da pesquisa incluam dados para objetos excluídos. Lembre-se de que esses controles são incluídos automaticamente na implementação do ADSI.

 

 