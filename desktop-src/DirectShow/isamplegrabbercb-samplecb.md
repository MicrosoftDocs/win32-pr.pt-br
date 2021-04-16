---
description: O método SampleCB é um método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Método ISampleGrabberCB:: SampleCB (QEdit. h)'
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
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782227"
---
# <a name="isamplegrabbercbsamplecb-method"></a>Método ISampleGrabberCB:: SampleCB

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

*Exemplo de* 
</dt> <dd>

Hora de início do exemplo, em segundos.

</dd> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se tiver êxito ou um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para configurar o retorno de chamada, chame [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




