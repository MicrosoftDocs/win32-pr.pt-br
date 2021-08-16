---
description: O método SampleCB é um método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: Método ISampleGrabberCB::SampleCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817508"
---
# <a name="isamplegrabbercbsamplecb-method"></a>Método ISampleGrabberCB::SampleCB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SampleCB` método é um método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SampleTime* 
</dt> <dd>

Hora de início do exemplo, em segundos.

</dd> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um **código de erro HRESULT** caso contrário.

## <a name="remarks"></a>Comentários

Para configurar o retorno de chamada, chame [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**ISampleGrabberCB Interface**](isamplegrabbercb.md)
</dt> </dl>

 

 




