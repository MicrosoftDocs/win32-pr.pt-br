---
description: Define o exemplo para a origem do fluxo de mídia.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Método IMFMediaStreamSourceSampleRequest:: setsample'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 80430e7902f4511e85c1b472f967aec6b6cc690f1d98ca14f5c883b600e1b250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957856"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a>Método IMFMediaStreamSourceSampleRequest:: setsample

Define o exemplo para a origem do fluxo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

O exemplo para a origem do fluxo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                       |
| INSERI<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaStreamSourceSampleRequest**](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




