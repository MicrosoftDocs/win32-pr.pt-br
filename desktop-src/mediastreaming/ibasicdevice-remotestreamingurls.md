---
title: Método IBasicDevice RemoteStreamingUrls
description: Retorna um vetor de URLs de streaming remota.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API de streaming de mídia do método RemoteStreamingUrls
- API de streaming de mídia do método RemoteStreamingUrls, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método RemoteStreamingUrls
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d98d908cb582c0c2885a9b24a0a525f1e719c82bdffe20e74597ca5fc262a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972325"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a>Método IBasicDevice:: RemoteStreamingUrls

Retorna um vetor de URLs de streaming remota.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe uma coleção enumerável de ponteiros para URLs de streaming remota.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





