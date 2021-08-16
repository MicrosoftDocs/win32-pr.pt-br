---
description: Escolha um método de menu de atalho estático ou dinâmico ao implementar um formato de arquivo personalizado no shell Windows.
title: Escolhendo um método de menu de atalho estático ou dinâmico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c910407dbd9de9f12853973f9891fe092a0603ca50a03e59183697b0f92b07e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968315"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Escolhendo um método de menu de atalho estático ou dinâmico

Este tópico é organizado da seguinte forma:

-   [Escolher um método de verbo](#choose-a-verb-method)
    -   [Métodos de verbo estático](#static-verb-methods)
    -   [Métodos de verbo dinâmico preferenciais](#preferred-dynamic-verb-methods)
    -   [Métodos de verbo dinâmico desacentados](#discouraged-dynamic-verb-methods)
-   [Estender um menu de atalho](#extend-a-shortcut-menu)
-   [Suporte para métodos verbais por sistema operacional](#support-for-verb-methods-by-operating-system)
-   [Tópicos relacionados](#related-topics)

## <a name="choose-a-verb-method"></a>Escolher um método de verbo

É fortemente incentivado que você implemente um menu de atalho usando um dos métodos verbais estáticos.

### <a name="static-verb-methods"></a>Métodos de verbo estático

Verbos estáticos são os verbos mais simples a implementar, mas ainda fornecem funcionalidade avançada. Sempre escolha o método de menu de atalho mais simples que atenda às suas necessidades.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verbo estático</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess com</strong></a> parâmetros de linha de comando</td>
<td>Esse é o meio mais simples e familiar de implementar um verbo estático. Um processo é invocado por meio de uma chamada para a função <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> com os arquivos selecionados e todos os parâmetros opcionais passados como a linha de comando. Isso abre o arquivo ou a pasta.<br/> Esse método tem as seguintes limitações:
<ul>
<li>O comprimento da linha de comando é limitado a 2.000 caracteres, o que limita o número de itens que o verbo pode manipular.</li>
<li>Só pode ser usado com itens do sistema de arquivos.</li>
<li>Não habilita o re uso de um processo já em execução.</li>
<li>Requer que um executável seja instalado para manipular o verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Uma ativação de verbo baseada em COM significa que dá suporte à ativação in-proc ou out-of-proc. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget também</strong></a> dá suporte ao re uso de um manipulador já em execução quando a interface <strong>IDropTarget</strong> é implementada por um servidor local. Ele também expressa perfeitamente os itens por meio do objeto de dados marshaled e fornece uma referência à cadeia de sites de invocação para que você possa interagir com o invocador por meio do <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService.</strong></a></td>
</tr>
<tr class="odd">
<td>Windows 7 e posterior: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>O método de implementação mais direto. Como esse é um método de invocação baseado em COM (como DropTarget), essa interface dá suporte à ativação in-proc e out-of-proc. O verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e, opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Os itens são passados diretamente como uma matriz de itens do Shell e mais dos parâmetros do invocador estão disponíveis para a implementação do verbo, incluindo o ponto de invocação, o estado do teclado e assim por diante.</td>
</tr>
<tr class="even">
<td>Windows 7 e posteriores:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Permite que fontes de dados que fornecem seus comandos de módulo de comando por <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>meio de IExplorerCommandProvider</strong></a> usem esses comandos como verbos em um menu de atalho. Como essa interface dá suporte apenas à ativação em processo, é recomendável usar por fontes de dados do Shell que precisam compartilhar a implementação entre comandos e menus de atalho.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) é um híbrido entre um verbo estático e dinâmico. **IExplorerCommand** foi declarado no Windows Vista, mas sua capacidade de implementar um verbo em um menu de atalho é nova para Windows 7.

 

Para obter mais informações sobre [**consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell para atributos de associação de arquivo, consulte [Tipos percebidos e Registro de aplicativo](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Métodos de verbo dinâmico preferenciais

Os seguintes métodos de verbo dinâmico são preferenciais:



| Tipo de verbo                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo estático (listado na tabela anterior) + Sintaxe de Consulta Avançada (AQS)                  | Essa opção obtém visibilidade de verbo dinâmico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 e posterior: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Essa opção permite uma implementação comum de verbos e comandos do explorer que são exibidos no módulo de comando no Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 e posterior: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático | Essa opção também obtém visibilidade de verbo dinâmico. É um modelo híbrido em que um manipulador em processo simples é usado para calcular se um determinado verbo estático deve ser displyed. Isso pode ser aplicado a todos os métodos de implementação de verbo estático para obter um comportamento dinâmico e minimizar a exposição da lógica em processo. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) tem a vantagem de executar em um thread em segundo plano e, assim, evita travas na interface do usuário. É consideravelmente mais simples do que [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) |



 

### <a name="discouraged-dynamic-verb-methods"></a>Métodos de verbo dinâmico desacentados

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é o método mais poderoso, mas também o método mais complicado de implementar. Ele se baseia em objetos COM em processo que são executados no thread do chamador, que geralmente Windows Explorer, mas pode ser qualquer aplicativo que hospeda os itens. **IContextMenu dá** suporte à visibilidade, à ordenação e ao desenho personalizado do verbo. Alguns desses recursos foram adicionados aos recursos verbais estáticos, como um ícone a ser associado a um comando, e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para lidar com visibilidade.

Se você tiver que estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas em Personalização de um menu de atalho usando [verbos dinâmicos.](shortcut-menu-using-dynamic-verbs.md)

## <a name="extend-a-shortcut-menu"></a>Estender um menu de atalho

Depois de escolher um método de verbo, você pode estender um menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo. Para obter mais informações, consulte [Criando manipuladores de menu de contexto](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Suporte para métodos verbais por sistema operacional

O suporte para métodos de invocação de verbo por sistema operacional está listado na tabela a seguir.



| Método Verb          | Windows XP | Windows Vista | Windows 7 e além |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| Executecommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e vários verbos de seleção](verbs-best-practices.md)
</dt> <dt>

[Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
</dt> <dt>

[Personalização de um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Referência de menu de atalho](context-menu-reference.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> </dl>

 

 
