---
title: Método ContentType IDeviceIcon
description: Recupera o tipo de conteúdo do ícone.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API de streaming de mídia do método ContentType
- API de streaming de mídia do método ContentType, interface IDeviceIcon
- API de streaming de mídia da interface IDeviceIcon, método ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823690"
---
# <a name="ideviceiconcontenttype-method"></a>Método IDeviceIcon:: ContentType

Recupera o tipo de conteúdo do ícone.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe um ponteiro para o tipo de conteúdo do ícone.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

