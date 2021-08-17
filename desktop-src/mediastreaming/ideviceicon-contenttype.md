---
title: Método ContentType IDeviceIcon
description: Recupera o tipo de conteúdo do ícone.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API de Streaming de Mídia do método ContentType
- Api de Streaming de Mídia do método ContentType, interface IDeviceIcon
- API de Streaming de Mídia da interface IDeviceIcon, método ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8fb9cb639381b60bb59965d12ce3f0545daf6d2725cde69d3dea3dee589f8f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461737"
---
# <a name="ideviceiconcontenttype-method"></a>Método IDeviceIcon::ContentType

Recupera o tipo de conteúdo do ícone.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para o tipo de conteúdo do ícone.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

