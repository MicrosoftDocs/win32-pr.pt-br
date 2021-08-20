---
description: A interface IAMTimelineGroup define e recupera propriedades em grupos no DES (DirectShow Editing Services). Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições, que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio. Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface IAMTimelineComp. Uma linha do tempo pode conter vários grupos. Cada grupo tem os seguintes atributos. Um tipo de mídia associado. A taxa de quadros na qual o grupo renderiza, em quadros por segundo (FPS). Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração FPS do grupo. Um nível de prioridade, para escrever arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois fluxos de vídeo). Para criar um objeto de grupo, chame IAMTimeline::CreateEmptyNode com o valor TIMELINE \_ MAJOR \_ TYPE \_ GROUP. Você pode consultar o ponteiro IAMTimelineObj retornado para a interface IAMTimelineGroup.
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interface IAMTimelineGroup (Qedit.h)
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
ms.openlocfilehash: 9356e3edef0b61c119ec4cca774e9ec5976ac3732e0f0a508d103bc22bb0fef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155502"
---
# <a name="iamtimelinegroup-interface"></a>Interface IAMTimelineGroup

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IAMTimelineGroup` interface define e recupera propriedades em grupos DirectShow [DES (Serviços](directshow-editing-services.md) de Edição).

Um grupo contém uma ou mais faixas e, possivelmente, uma ou mais composições, que, por sua vez, contêm clipes de origem de um tipo uniforme, como vídeo ou áudio. Os grupos são as composições mais altas em uma linha do tempo e também expõem a interface [**IAMTimelineComp.**](iamtimelinecomp.md) Uma linha do tempo pode conter vários grupos.

Cada grupo tem os seguintes atributos.

-   Um tipo de mídia associado.
-   A taxa de quadros na qual o grupo renderiza, em quadros por segundo (FPS). Todas as edições ocorrem em um tempo arredondado para o limite de quadro mais próximo, conforme definido pela configuração FPS do grupo.
-   Um nível de prioridade, para escrever arquivos com vários fluxos do mesmo tipo de mídia (por exemplo, um arquivo AVI de dois fluxos de vídeo).

Para criar um objeto de grupo, chame [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor TIMELINE \_ MAJOR TYPE \_ \_ GROUP. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a interface **IAMTimelineGroup.**

## <a name="members"></a>Membros

A interface **IAMTimelineGroup** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineGroup** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineGroup** tem esses métodos.



| Método                                                                            | Descrição                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Sem suporte.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Recupera o nome definido pelo aplicativo do grupo.<br/>                                 |
| [**Getmediatype**](iamtimelinegroup-getmediatype.md)                             | Recupera o tipo de mídia descompactado para o grupo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera o número de quadros renderizados com antecedência durante a versão prévia.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera a taxa de quadros de saída desse grupo.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera o modo de visualização do grupo.<br/>                                            |
| [**Getpriority**](iamtimelinegroup-getpriority.md)                               | Recupera a prioridade do grupo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera o formato de compactação atual para recompactação inteligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Recupera a linha do tempo à qual este grupo pertence.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Sem suporte.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina se um formato de compactação inteligente foi definido para o grupo.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Define o nome definido pelo aplicativo do grupo.<br/>                                      |
| [**Setmediatype**](iamtimelinegroup-setmediatype.md)                             | Define o tipo de mídia descompactado para o grupo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Especifica o tipo de mídia de grupo, para clientes de Automação.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Especifica o número de quadros renderizados com antecedência durante a versão prévia.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Define a taxa de quadros de saída descompactada para esse grupo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Define o modo de visualização para o grupo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Especifica um formato de compactação a ser usado para recompactação inteligente.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | Sem suporte.<br/>                                                                       |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
