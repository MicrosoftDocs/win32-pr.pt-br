---
description: A interface IAMTimelineComp insere ou recupera faixas virtuais em uma composição nos serviços de edição do DirectShow (DES). Uma composição é uma coleção de camadas que atua como uma faixa única e composta.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interface IAMTimelineComp (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775614"
---
# <a name="iamtimelinecomp-interface"></a>Interface IAMTimelineComp

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A interface **IAMTimelineComp** insere ou recupera faixas virtuais em uma composição nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

Uma composição é uma coleção de camadas que atua como uma *faixa* única e composta. Por exemplo, uma composição que contém duas faixas com uma transição entre elas atua como uma única faixa com a transição precomposta. Uma composição deve conter mídia de apenas um tipo (como áudio ou vídeo), mas essa limitação não é imposta. Um *controle virtual* é qualquer objeto que possa residir em uma composição, incluindo faixas e outras composições.

Os nós mais altos na linha do tempo são *grupos*. Os grupos implementam a `IAMTimelineComp` interface e a interface [**IAMTimelineGroup**](iamtimelinegroup.md) .

Para criar um objeto de composição, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ Major \_ tipo \_ composto. Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineComp` interface. Para obter mais informações, consulte [o modelo de linha do tempo](the-timeline-model.md) e [construindo uma linha do tempo](constructing-a-timeline.md).

## <a name="members"></a>Membros

A interface **IAMTimelineComp** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineComp** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMTimelineComp** tem esses métodos.



| Método                                                                       | Descrição                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Recupera a próxima faixa virtual após uma faixa virtual especificada.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a *n* º de faixa virtual dessa ordem.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | Não há suporte.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Recupera a faixa virtual na prioridade especificada.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Recupera o número de faixas virtuais contidas na composição.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Insere uma faixa virtual na composição na prioridade especificada.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Alterna os níveis de prioridade de duas faixas.<br/>                                                                                                    |



 

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



 

 
