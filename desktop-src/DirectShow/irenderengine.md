---
description: 'a interface IRenderEngine renderiza um projeto de serviços de edição DirectShow (DES) construindo um grafo de filtro de uma linha do tempo. O DES fornece dois componentes que implementam essa interface: o mecanismo de renderização básico cria uma saída não compactada.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interface IRenderEngine (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051306"
---
# <a name="irenderengine-interface"></a>Interface IRenderEngine

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

a `IRenderEngine` interface renderiza um projeto de [serviços de edição DirectShow](directshow-editing-services.md) (DES) construindo um grafo de filtro de uma linha do tempo.

O DES fornece dois componentes que implementam essa interface:

-   O *mecanismo de renderização básico* cria uma saída não compactada. Você pode usar a saída para visualização ou circulá-la por meio de filtros de compactação e gravá-la em um arquivo.
-   O *mecanismo de processamento inteligente* cria uma saída compactada, usando a *recompactação inteligente*. Com a recompactação inteligente, um arquivo de origem será recompactado somente se seu formato for diferente do formato de saída. Uma fonte com um formato correspondente é gravada diretamente no arquivo de saída. Dependendo do cenário, a recompactação inteligente pode melhorar muito o tempo de renderização.

O mecanismo de processamento inteligente também dá suporte à interface [**ISmartRenderEngine**](ismartrenderengine.md) .

Embora um aplicativo possa criar um gráfico de filtro e passá-lo para um mecanismo de renderização, o cenário típico é que o mecanismo de renderização crie o gráfico de filtro. Criar o grafo é um processo de duas etapas. Primeiro, compile o front-end chamando o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . Em seguida, conecte os Pins de saída no front-end aos filtros de renderização desejados:

-   Renderizadores de vídeo e áudio para visualização ou
-   Compactadores, multiplexadores e gravadores de arquivo para gerar a saída final.

## <a name="members"></a>Membros

A interface **IRenderEngine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRenderEngine** tem esses métodos.



| Método                                                                             | Descrição                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Compromisso**](irenderengine-commit.md)                                             | Não implementado.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Cria o front-end do grafo de filtro a partir da linha do tempo atual.<br/>        |
| [**Anulação confirmação**](irenderengine-decommit.md)                                         | Não implementado.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | Sem suporte.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Não implementado.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Recupera o gráfico de filtro que o mecanismo de processamento construiu, se houver.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Recupera o pino de saída para o grupo especificado.<br/>                          |
| [**Gettimelineobject**](irenderengine-gettimelineobject.md)                       | Recupera a linha do tempo que o mecanismo de processamento está usando no momento.<br/>          |
| [**Getvendor**](irenderengine-getvendorstring.md)                           | Recupera a cadeia de caracteres do fornecedor.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Cria a parte de visualização do grafo de filtro.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Descarta o grafo de filtro do mecanismo de processamento e todos os objetos associados.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Define o nível de reconexão dinâmica durante a renderização.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Especifica um grafo de filtro para o mecanismo de renderização usar.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | Sem suporte.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Sem suporte.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Define o intervalo de tempo a ser renderizado.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Define o intervalo de tempo a ser renderizado, como um **duplo**.<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | Sem suporte.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Especifica como o mecanismo de renderização valida nomes de arquivo.<br/>                      |
| [**Settimelineobject**](irenderengine-settimelineobject.md)                       | Define a linha do tempo para o mecanismo de renderização usar.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | Sem suporte.<br/>                                                             |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Renderizando um Project](rendering-a-project.md)
</dt> </dl>

 

 
