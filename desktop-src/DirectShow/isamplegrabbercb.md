---
description: 'A interface ISampleGrabberCB fornece métodos de retorno de chamada para o método ISampleGrabber:: SetCallback. Se seu aplicativo chamar esse método, ele deverá implementar essa interface. Para obter mais informações, consulte ISampleGrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interface ISampleGrabberCB (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 822eef97ebd2ff169631f0e4d83cdfe3417388389e112851f5e77dcd7216acfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817498"
---
# <a name="isamplegrabbercb-interface"></a>Interface ISampleGrabberCB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `ISampleGrabberCB` interface fornece métodos de retorno de chamada para o método [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) . Se seu aplicativo chamar esse método, ele deverá implementar essa interface. Para obter mais informações, consulte [**ISampleGrabber**](isamplegrabber.md).

## <a name="members"></a>Membros

A interface **ISampleGrabberCB** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabberCB** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISampleGrabberCB** tem esses métodos.



| Método                                        | Descrição                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | Método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | Método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.<br/>  |



 

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



 

 
