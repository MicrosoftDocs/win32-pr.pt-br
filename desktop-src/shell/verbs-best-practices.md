---
description: entenda as práticas recomendadas para manipuladores de menu de atalho e vários verbos ao implementar um formato de arquivo personalizado no Shell de Windows.
title: Práticas recomendadas para manipuladores de menu de atalho e vários verbos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cb44eaf0b3e1c63b9f900f398a218051710f857a7b628d454daa87679d557ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675500"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Práticas recomendadas para manipuladores de menu de atalho e vários verbos

Este tópico é organizado da seguinte maneira:

-   [Práticas recomendadas](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Práticas recomendadas para implementações de verbo](#best-practices-for-verb-implementations)
-   [Práticas recomendadas para verbos de seleção múltipla](#best-practices-for-multiple-selection-verbs)
    -   [Seleções heterogêneas](#heterogenous-selections)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices"></a>Práticas Recomendadas

O verbo estático é um verbo mais simples para implementar e fornecer funcionalidade avançada. Recomendamos que você implemente um verbo usando um dos métodos de verbo estáticos.

### <a name="best-practices-for-verb-implementations"></a>Práticas recomendadas para implementações de verbo

A lista a seguir representa as práticas recomendadas para implementações de verbo:

-   Sempre escolha o método de verbo mais simples que atenda às suas necessidades.
-   Use um método verbo estático, se possível.
-   Não execute operações com uso intensivo de recursos ou e/s no thread da interface do usuário. Ambos os [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) precisam ser muito conservadores no trabalho que eles executam. [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) deve ser executado em outro processo ou você deve criar um novo thread para evitar o bloqueio do chamador.
-   Prefixe os verbos com o nome ISV (fornecedor independente de software) da seguinte maneira, `ISVName.verb` . O uso de nomes não qualificados pode resultar em colisões com vários ISVs que escolhem o mesmo nome de verbo.
-   Sempre use um ProgID específico do aplicativo. Como alguns tipos de item não usam esse mapeamento, há uma necessidade de nomes exclusivos de fornecedor.
-   Posicione a interface do usuário em relação ao método de invocação, mas não execute em um thread do chamador.
-   Não aceite o valor de retorno **S \_ OK** para verbos canônicos passados para o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Isso faz com que uma falha para a implementação de verbo real seja invocada e retorna um código de falha para verbos canônicos. Se você não der suporte a verbos canônicos, retorne a falha quando um valor de HIWORD (lpVerb) diferente de zero for encontrado.
-   Evite o uso de **rundll32.exe** como o host para o verbo.
-   Ao implementar [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , certifique-se de retornar o número de verbos que foram adicionados ao menu por meio do valor **HRESULT** usando a macro ResultFromShort.
-   Se você se registrar em uma das seguintes entradas de chave do registro, tenha cuidado e certifique-se de registrar seu manipulador no tipo mais específico para reduzir as consequências possivelmente indesejadas:
    -   **\_raiz de classes hKey \_\\\***
    -   **\_AllFileSystemObjects de \_ raiz de classes hKey \\**
    -   **\_ \_ Pasta raiz de classes hKey \\**
    -   **\_ \_ Diretório raiz de classes hKey \\**
-   Defina a chave **MayChangeDefaultMenu** somente se você antecipar que talvez precise alterar o verbo padrão no menu de atalho. Se o manipulador não alterar o verbo padrão, você não deverá definir essa chave porque isso faz com que o sistema carregue sua DLL desnecessariamente.
-   Minimize o trabalho que você executa em [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Para manipuladores de menu de atalho, Capture o objeto de dados passado para **IShellExtInit:: Initialize** e, em seguida, processe-o em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)ou [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Práticas recomendadas para verbos de seleção múltipla

Como o número de itens em um cenário de verbo de seleção múltipla pode ser grande, é importante que você considere as implicações de desempenho de suas implementações de verbo. Por exemplo, quando um usuário procura por " \* " sobre um escopo que inclui um grande número de itens e clica em **selecionar tudo** e clica com o botão direito do mouse, o verbo é apresentado com uma seleção que pode ter milhares de itens. Como resultado, os verbos devem considerar apenas o primeiro item na seleção e a contagem geral de itens. O primeiro item é definido como o item na parte superior da exibição ou o item em que o usuário clicou pela primeira vez.

no Windows 7 e posterior, o número de itens passados para um verbo é limitado a 16 quando um menu de atalho é consultado. Em seguida, o verbo é recriado e reinicializado com a seleção completa quando esse verbo é invocado.

Isso é apropriado em alguns casos para considerar um pequeno número de itens fixos. Por exemplo, é apropriado para um verbo "diff" para considerar apenas os dois primeiros itens. Em geral, você não precisa testar todos os itens na seleção para ver se ele é um determinado tipo ou consultar cada item na seleção para suas propriedades. Observe o primeiro item e decida se é apropriado adicionar o verbo.

### <a name="heterogenous-selections"></a>Seleções heterogêneas

Os verbos otimistas são adicionados automaticamente ao caso de várias seleções, supondo que os itens não inspecionados possam ser manipulados pelo verbo. Por outro lado, os verbos pessimistas não são adicionados quando a seleção contém itens não inspecionados e são adicionados somente em casos em que o número de itens é pequeno.

Os verbos do estilo do jogador devem ser otimistas e ignorar silenciosamente os itens que não são manipulados. Se uma falha de atuar em itens puder causar perda ou confusão de dados, o verbo deverá avisar os usuários sobre os itens que não podem ser processados. Por exemplo, um verbo de "backup" deve indicar que não foi possível fazer backup de alguns itens.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
</dt> <dt>

[Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> <dt>

[Referência do menu de atalho](context-menu-reference.md)
</dt> </dl>

 

 



