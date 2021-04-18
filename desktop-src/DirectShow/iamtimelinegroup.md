---
description: 'A interface IAMTimelineGroup define e recupera propriedades em grupos nos serviços de edição do DirectShow (DES). Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio. Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface IAMTimelineComp. Uma linha do tempo pode conter vários grupos. Cada grupo tem os seguintes atributos. Um tipo de mídia associado. A taxa de quadros na qual o grupo é renderizado, em quadros por segundo (FPS). Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração de FPS do grupo. Um nível de prioridade, para gravar arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois vídeos). Para criar um objeto de grupo, chame IAMTimeline:: CreateEmptyNode com o valor TIMELINE \_ principal \_ tipo \_ grupo. Você pode consultar o ponteiro IAMTimelineObj retornado para a interface IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interface IAMTimelineGroup (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810399"
---
# <a name="iamtimelinegroup-interface"></a>Interface IAMTimelineGroup

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineGroup` interface define e recupera propriedades em grupos nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio. Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface [**IAMTimelineComp**](iamtimelinecomp.md) . Uma linha do tempo pode conter vários grupos.

Cada grupo tem os seguintes atributos.

-   Um tipo de mídia associado.
-   A taxa de quadros na qual o grupo é renderizado, em quadros por segundo (FPS). Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração de FPS do grupo.
-   Um nível de prioridade, para gravar arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois vídeos).

Para criar um objeto de grupo, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor Timeline \_ principal \_ tipo \_ grupo. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a interface **IAMTimelineGroup** .

## <a name="members"></a>Membros

A interface **IAMTimelineGroup** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineGroup** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineGroup** tem esses métodos.



| Método                                                                            | Descrição                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Não há suporte.<br/>                                                                       |
| [**Getgroupname**](iamtimelinegroup-getgroupname.md)                             | Recupera o nome definido pelo aplicativo do grupo.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Recupera o tipo de mídia descompactado para o grupo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera o número de quadros renderizados antecipadamente durante a visualização.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera a taxa de quadros de saída deste grupo.<br/>                                       |
| [**Getpreviewmode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera o modo de visualização do grupo.<br/>                                            |
| [**Getanteriority**](iamtimelinegroup-getpriority.md)                               | Recupera a prioridade do grupo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera o formato de compactação atual para a recompactação inteligente.<br/>                    |
| [**GetTimer**](iamtimelinegroup-gettimeline.md)                               | Recupera a linha do tempo à qual este grupo pertence.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Não há suporte.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina se um formato de compactação inteligente foi definido para o grupo.<br/>                 |
| [**Setgroupname**](iamtimelinegroup-setgroupname.md)                             | Define o nome definido pelo aplicativo do grupo.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Define o tipo de mídia descompactado para o grupo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Especifica o tipo de mídia do grupo, para clientes de automação.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Especifica o número de quadros renderizados antecipadamente durante a visualização.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Define a taxa de quadros de saída não compactados para esse grupo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Define o modo de visualização para o grupo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Especifica um formato de compactação a ser usado para a recompactação inteligente.<br/>                       |
| [**SetTimer**](iamtimelinegroup-settimeline.md)                               | Não há suporte.<br/>                                                                       |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
