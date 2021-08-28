---
description: o gerenciador de escopo de rastreamento (CSM) permite que você defina regras de escopo que incluem ou excluem URLs do escopo de rastreamento de pesquisa Windows.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Gerenciando regras de escopo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134e4241e9dcd66e468935ae56a4029a51a96c37
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880220"
---
# <a name="managing-scope-rules"></a>Gerenciando regras de escopo

o gerenciador de escopo de rastreamento (CSM) permite que você defina regras de escopo que incluem ou excluem URLs do escopo de rastreamento de pesquisa Windows.

O CSM permite que você faça o seguinte:

-   Adicionar novas regras de escopo ao conjunto de regras de trabalho
-   Remover regras de escopo existentes
-   Enumerar regras de escopo padrão
-   Descobrir se uma determinada URL está incluída ou excluída do escopo de rastreamento ou se tem uma regra de escopo pai ou filho

 

Este tópico abrange os seguintes assuntos:

-   [Sobre regras de escopo](#about-scope-rules)
-   [Antes de começar](#before-you-begin)
-   [Adicionando regras de escopo](#adding-scope-rules)
    -   [Observações sobre regras de usuário](#notes-on-user-rules)
-   [Removendo regras de escopo](#removing-scope-rules)
-   [Revertendo para regras padrão](#reverting-to-default-rules)
-   [Enumerando regras de escopo](#enumerating-scope-rules)
-   [Regras de escopo de rastreamento](#tracing-scope-rules)
-   [Tópicos relacionados](#related-topics)

## <a name="about-scope-rules"></a>Sobre regras de escopo

Uma regra de escopo é uma regra que inclui ou exclui URLs em uma raiz de pesquisa de serem rastreadas e indexadas. As regras de inclusão fazem com que o indexador inclua essa URL no escopo Scrawl e as regras de exclusão fazem com que o indexador exclua essa URL (e seus filhos) do escopo de rastreamento.

Por exemplo, suponha que você tenha instalado um novo aplicativo cujos arquivos de dados estejam localizados na pasta WorkteamA \\ ProjectFiles em um computador local. Suponha que você deseja que tudo esteja dentro da pasta ProjectFiles indexada, exceto por itens nos protótipos de subpasta. Nessa situação, você precisaria de uma regra de inclusão para myPH:///C: \\ WorkteamA \\ ProjectFiles \\ e uma regra de exclusão para \\ os \\ protótipos myPH:///C: WorkteamA ProjectFiles \\ \\ .

Há três tipos de regras, com a seguinte ordem de precedência:

1.  As regras de Política de Grupo são definidas por administradores e podem substituir todas as outras regras.
2.  as regras de usuário são definidas por usuários modificando o escopo na interface do usuário de opções de Windows Search. Os usuários ou outros aplicativos podem remover todas as regras de usuário e reverter para as regras padrão.
3.  As regras padrão normalmente são definidas por um aplicativo para definir um escopo padrão. Por exemplo, regras padrão podem ser definidas quando um novo manipulador de protocolo ou contêiner é adicionado ao sistema.

Juntos, esses tipos de regras incluem o *conjunto de regras de trabalho* do qual o Gerenciador de escopo de rastreamento (CSM) gera a lista completa de URLs a serem rastreadas. Embora as regras padrão possam ser substituídas pelas regras de diretiva de grupo e por regras de usuário, elas são mantidas em seu próprio conjunto de regras padrão, que pode ser revertido a qualquer momento. O indexador rastreia as URLs do conjunto de regras de trabalho e adiciona itens, propriedades e conteúdo ao catálogo.

> [!Note]  
> Os usuários com acesso ao painel de controle podem modificar as regras por meio dessa interface. Portanto, os aplicativos que oferecem gerenciamento de escopo sempre devem obter as regras diretamente do CSM usando os métodos de enumeração em vez de depender de uma cópia salva das regras do usuário.

 

As regras de exclusão podem definir URLs de padrão com o caractere curinga ' \* '; por exemplo: file:///C: \\ projecta \\ \* \\ . Uma regra de exclusão que usa esse padrão impede que o indexador rastreie todas as pastas no diretório projecta. Para obter um exemplo mais complicado, suponha que haja uma regra de inclusão para file:///C: \\ projecta \\ e uma regra de padrão de exclusão para \\ \\ \* \\ os dados de \\ file:///C: projecta \* . Nesse caso, o indexador rastrearia itens em:

-   C: \\ projetoa\\
-   C: \\ projecta \\ **versão** \\ testfiles\\
-   C: \\ \\ **dados \\ temporários** do projecta versão \\\\

Mas o indexador não rastrearia itens em:

-   C: \\ dados do projecta \\ **versão** \\\\

 

## <a name="before-you-begin"></a>Antes de começar

Antes de usar qualquer uma das interfaces do Gerenciador de escopo de rastreamento, você deve executar as seguintes etapas de pré-requisito:

1.  Crie o objeto **CSearchManager** e obtenha sua interface **ISearchManager** .
2.  Chame **ISearchManager:: getCatalog** para "SystemIndex" para obter uma instância da interface **ISearchCatalogManager** .
3.  Chame **ISearchCatalogManager:: GetCrawlScopeManager** para obter uma instância da interface **ISearchCrawlScopeManager** .

Depois de fazer alterações no Gerenciador de escopo de rastreamento, você deve chamar o método [**ISearchCrawlScopeManager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) . Esse método não usa parâmetros e retorna S \_ OK em caso de êxito.

 

## <a name="adding-scope-rules"></a>Adicionando regras de escopo

As regras de trabalho definidas para o CSM incluem regras de usuário e padrão, bem como todas as regras forçadas pela política de grupo. As regras de usuário são configuradas por usuários em uma interface do usuário e as regras padrão podem ser definidas por qualquer um dos seguintes:

-   Diretivas de Grupo implementadas por um administrador do sistema (elas não usam a interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .)
-   a instalação ou atualização de um aplicativo como Windows pesquisa ou um manipulador de protocolo
-   Um aplicativo de instalação para a adição de um novo armazenamento de dados ou contêiner

O [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornece dois métodos para adicionar novas regras de escopo, conforme descrito na tabela a seguir. Os caminhos para regras de inclusão para o sistema de arquivos devem terminar com uma barra invertida ' \\ ' (por exemplo, file:///C: \\ files \\ ) e os caminhos para regras de exclusão devem terminar com um asterisco (por exemplo, file:///c: \\ files \\ \* ). Somente as regras de exclusão podem conter URLs de padrão. Além disso, é recomendável incluir SIDs (identificadores de segurança) dos usuários em caminhos, para maior segurança. Os caminhos por usuário são mais seguros, pois as consultas seriam executadas em um processo por usuário, garantindo que um usuário não possa ver itens indexados da caixa de entrada de outro usuário, por exemplo.

A tabela a seguir descreve os métodos da interface ISearchCrawlScopeManager usada para adicionar novas regras de escopo.



| Método                                                                              | Descrição                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Adiciona uma regra para uma URL, conforme especificado pelo usuário. Essas regras substituem as regras padrão. Use esse método se você tiver implementado uma interface do usuário que permite aos usuários gerenciar suas próprias regras e URLs de escopo.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Adiciona uma regra para uma URL, conforme especificado por outro aplicativo, como um manipulador de protocolo. Use esse método quando você tiver implementado um novo manipulador de protocolo ou adicionado um novo armazenamento de dados. Essas regras podem ser substituídas pelas regras do usuário. |



 

Cada método usa uma URL para um local indexável e sinalizadores que determinam se a URL deve ser incluída ou excluída. O parâmetro *fFollowFlags* é reservado para uso futuro. Quando você adiciona uma nova regra de escopo e o Gerenciador de escopo de rastreamento determina que a regra já existe (com base na URL ou no padrão fornecido), o conjunto de regras de trabalho é atualizado para que (1) a regra antiga seja substituída pela nova regra e (2) qualquer regra de usuário que contradiz que ela seja removida.

**Dica:** Embora a raiz file://seja incluída por padrão no escopo do rastreamento, os arquivos de programa não são indexados por padrão. Portanto, os aplicativos com dados salvos no diretório arquivos de programas precisam adicionar seu local como uma regra padrão.

### <a name="notes-on-user-rules"></a>Observações sobre regras de usuário

Se uma nova regra de usuário for igual a uma regra padrão existente, a nova regra de usuário substituirá a regra padrão no conjunto de regras de trabalho. Se a nova regra de usuário for a mesma que uma regra de usuário existente, a regra de usuário antiga será substituída.

A definição do sinalizador *fOverrideChildren* tem os seguintes resultados no conjunto de regras de trabalho:

-   **Verdadeiro** resulta na remoção de todas as regras filho do conjunto de regras de trabalho (regras de usuário e regras padrão).
-   FALSO resulta na readição às regras de trabalho defina todas as regras padrão que são filhos da nova regra de usuário. Se uma regra padrão filho for uma inclusão e a nova regra de usuário for uma exclusão, a regra padrão será alterada para uma regra de usuário de inclusão.

 

## <a name="removing-scope-rules"></a>Removendo regras de escopo

Você pode usar a interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para remover uma regra de escopo do conjunto de regras de trabalho. Essa interface fornece os dois métodos a seguir para remover regras de escopo.



| Método                                                                                    | Descrição                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Remove uma regra de usuário para uma URL especificada do conjunto de regras de trabalho. Se a regra de usuário for uma duplicata ou substituir uma regra padrão, a regra padrão permanecerá no conjunto de regras de trabalho.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Remove uma regra padrão para uma URL especificada do conjunto de regras de trabalho e do conjunto de regras padrão. Depois de chamar esse método, não é possível reverter para essa regra padrão usando RevertToDefaultScopes. |



 

Cada método usa uma URL e um sinalizador que indica se a regra a ser removida é uma regra de inclusão ou exclusão. Esses métodos retornarão um erro se uma regra com essa URL e o sinalizador de inclusão/exclusão não for encontrado.

**Dica:** Se você quiser remover completamente um escopo do escopo do rastreamento, use o método [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) , que remove a raiz de pesquisa e todas as regras de escopo associadas. Fazer isso durante a desinstalação, por exemplo, é considerada a melhor prática.

Também é possível remover todas as substituições definidas pelo usuário de uma raiz de pesquisa e reverter para as regras de escopo padrão e raiz de pesquisa originais. Para obter mais informações, consulte a próxima seção.

> [!Note]  
> No Windows Vista, se os usuários são removidos por meio de Perfis de Usuário no Painel de Controle, o CSM remove todas as regras e raízes que incluem seu SID e remove seus itens indexados do catálogo. No Windows XP, você deve remover manualmente as raízes e as regras dos usuários.

 

 

## <a name="reverting-to-default-rules"></a>Revertendo para regras padrão

Reverter para regras padrão remove todas as regras de usuário para uma URL ou raiz e restaura todas as regras padrão para o conjunto de regras de trabalho. No entanto, ele não remove as regras definidas pela política de grupo. O [**método RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) não recebe parâmetros e retorna um código de erro se não for possível reverter para as regras padrão.

 

## <a name="enumerating-scope-rules"></a>Enumerando regras de escopo

O CSM enumera regras de escopo usando uma interface de enumerador de estilo COM padrão, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) . Você pode usar essa interface para enumerar regras de escopo para várias finalidades. Por exemplo, talvez você queira exibir todo o conjunto de regras de trabalho em uma interface do usuário ou descobrir se uma regra ou o filho de uma regra já está no escopo de rastreamento.

 

## <a name="tracing-scope-rules"></a>Regras de escopo de rastreamento

O CSM também permite que você determine se uma URL especificada está incluída no escopo de rastreamento e se ela tem uma regra de escopo pai ou filho. Você também pode descobrir por que uma URL é incluída ou excluída do escopo de rastreamento. Esses métodos não devem ser usados com URLs padrão.

A tabela a seguir descreve os métodos de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) usados para adicionar novas regras de escopo.



| Método                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Obtém a ID da versão da URL de inclusão pai. Você pode usar esse método para ver se o escopo pai foi alterado desde a última vez que você o verificou.<br/> Exemplo: se um aplicativo de email usar notificações gerenciadas pelo provedor, ele poderá obter a versão do escopo pai antes de fechar e verificar a versão novamente quando for aberta. Em seguida, o aplicativo pode determinar se precisa fazer push de um novo conjunto de notificações para o indexador.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Retornará **TRUE** se a URL especificada tiver uma regra filho (uma regra que se aplica a um filho em qualquer nível dentro de sua hierarquia de URL). <br/> Exemplo: se a URL for file:///C: Pasta , esse método retornará TRUE se o CSM tiver uma regra de escopo especificamente para \\ \\ file:///C:  \\ \\ Subpasta de Pasta \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Retornará **TRUE** se a URL especificada tiver uma regra pai (uma regra que se aplica a um pai em qualquer nível na hierarquia de URL).<br/> Exemplo: se a URL for file:///C: Subpasta de Pasta, esse método retornará TRUE se o CSM tiver uma regra de escopo especificamente \\ \\ para file:///C: Pasta  \\ \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Retornará **TRUE** se a URL especificada estiver incluída no escopo do rastreamento.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Retorna um valor da enumeração [**CLUSION \_ REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) explicando por que a URL está incluída ou excluída do escopo de rastreamento e recupera o valor **TRUE** se a URL estiver incluída no escopo de rastreamento. Esse método pode ajudá-lo a identificar conflitos em seu conjunto de regras de trabalho.                                                                                                                                       |



 

 

> [!Note]  
> Os [**métodos IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) e [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) determinam se a URL será rastreada com base apenas nas regras no CSM. Pode haver outros motivos pelos quais uma URL não está rastreada, como o bit FANCI que está sendo definido (ou seja, um usuário não tem permitido a indexação rápida na caixa de diálogo Propriedade da pasta.)

 

Se você acredita que um caminho de arquivo deve ser excluído, mas ele está listado como incluído, certifique-se de que as regras de exclusão terminem com " &lt; caminho &gt; \\ \* ". Se você acredita que um arquivo ou caminho de arquivo deve ser incluído, mas não está, verifique a configuração de bit FANCI para o arquivo ou caminho. Você pode fazer isso clicando com o botão direito do mouse no caminho do arquivo ou arquivo e selecionando Propriedades e, em seguida, verifique se a caixa de seleção Para pesquisa **rápida,** permita que o Serviço de Indexação indexe essa pasta está marcada. Se o caminho do arquivo ou do arquivo não estiver marcado para indexação aqui, ele não será indexado mesmo se estiver em uma regra de inclusão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Gerenciando raízes de pesquisa](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




