---
description: 'Este tópico é organizado da seguinte maneira:'
title: Escolhendo um método de menu de atalho estático ou dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011329"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Escolhendo um método de menu de atalho estático ou dinâmico

Este tópico é organizado da seguinte maneira:

-   [Escolher um método de verbo](#choose-a-verb-method)
    -   [Métodos de verbo estáticos](#static-verb-methods)
    -   [Métodos de verbo dinâmico preferenciais](#preferred-dynamic-verb-methods)
    -   [Métodos de verbo dinâmico desencorajados](#discouraged-dynamic-verb-methods)
-   [Estender um menu de atalho](#extend-a-shortcut-menu)
-   [Suporte para métodos de verbo por sistema operacional](#support-for-verb-methods-by-operating-system)
-   [Tópicos relacionados](#related-topics)

## <a name="choose-a-verb-method"></a>Escolher um método de verbo

É altamente recomendável que você implemente um menu de atalho usando um dos métodos de verbo estáticos.

### <a name="static-verb-methods"></a>Métodos de verbo estáticos

Verbos estáticos são os verbos mais simples de implementar, mas ainda fornecem funcionalidade avançada. Sempre escolha o método de menu de atalho mais simples que atenda às suas necessidades.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verbo estático</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> com parâmetros de linha de comando</td>
<td>Esse é o meio mais simples e mais familiar de implementar um verbo estático. Um processo é invocado por meio de uma chamada para a função <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> com os arquivos selecionados e os parâmetros opcionais passados como a linha de comando. Isso abre o arquivo ou a pasta.<br/> Esse método tem as seguintes limitações:
<ul>
<li>O comprimento da linha de comando é limitado a 2000 caracteres, o que limita o número de itens que o verbo pode manipular.</li>
<li>Só pode ser usado com itens do sistema de arquivos.</li>
<li>Não habilita a reutilização de um processo já em execução.</li>
<li>Requer que um executável seja instalado para manipular o verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Uma ativação de verbo baseada em COM significa que dá suporte à ativação em proc ou fora do processo. <strong>DropTarget</strong> / O <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> também dá suporte à reutilização de um manipulador já em execução quando a interface <strong>IDropTarget</strong> é implementada por um servidor local. Ele também expressa perfeitamente os itens por meio do objeto de dados marshaled e fornece uma referência à chamada de cadeia de sites para que você possa interagir com o chamador por meio do <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 e posterior: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>O método de implementação mais direto. Como esse é um método Invoke baseado em COM (como DropTarget), essa interface dá suporte à ativação no proc e fora do processo. O verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e, opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Os itens são passados diretamente como uma matriz de item de shell e mais dos parâmetros do chamador estão disponíveis para a implementação de verbo, incluindo o ponto de invocação, o estado do teclado e assim por diante.</td>
</tr>
<tr class="even">
<td>Windows 7 e posterior:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Habilita fontes de dados que fornecem seus comandos de módulo de comando por meio do <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> para usar esses comandos como verbos em um menu de atalho. Como essa interface dá suporte apenas à ativação em processo, é recomendável usar por fontes de dados do shell que precisam compartilhar a implementação entre comandos e menus de atalho.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) é um híbrido entre um verbo estático e o dinâmico. **IExplorerCommand** foi declarado no Windows Vista, mas sua capacidade de implementar um verbo em um menu de atalho é nova no Windows 7.

 

Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Métodos de verbo dinâmico preferenciais

Os métodos de verbo dinâmico a seguir são preferenciais:



| Tipo de verbo                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo estático (listado na tabela anterior) + sintaxe de consulta avançada (AQS)                  | Essa opção Obtém a visibilidade dinâmica de verbo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 e posterior: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Essa opção permite uma implementação comum de verbos e comandos do Explorer que são exibidos no módulo de comando no Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 e posterior: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático | Essa opção também obtém visibilidade dinâmica de verbo. É um modelo híbrido em que um manipulador no processo simples é usado para calcular se um determinado verbo estático deve ser exibido. Isso pode ser aplicado a todos os métodos de implementação de verbo estático para obter o comportamento dinâmico e minimizar a exposição da lógica em processo. O [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) tem a vantagem de executar em um thread em segundo plano e, assim, evita os bloqueios da interface do usuário. É consideravelmente mais simples do que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Métodos de verbo dinâmico desencorajados

O [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é o mais potente, mas também o método mais complicado para implementar. Ele se baseia em objetos COM em processo que são executados no thread do chamador, que geralmente o Windows Explorer, mas pode ser qualquer aplicativo que hospede os itens. O **IContextMenu** dá suporte à visibilidade de verbo, ordenação e desenho personalizado. Alguns desses recursos foram adicionados aos recursos de verbo estático, como um ícone a ser associado a um comando e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para lidar com a visibilidade.

Se você precisar estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas em [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Estender um menu de atalho

Depois de escolher um método de verbo, você pode estender um menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo. Para obter mais informações, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Suporte para métodos de verbo por sistema operacional

O suporte para métodos de invocação de verbo por sistema operacional está listado na tabela a seguir.



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | Windows XP | Windows Vista | Windows 7 e posterior |
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla](verbs-best-practices.md)
</dt> <dt>

[Criando manipuladores de menu de atalho](context-menu-handlers.md)
</dt> <dt>

[Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Referência do menu de atalho](context-menu-reference.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> </dl>

 

 
