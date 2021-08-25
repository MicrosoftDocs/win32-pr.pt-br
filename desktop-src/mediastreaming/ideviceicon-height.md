---
title: Método height IDeviceIcon
description: Recupera a altura do ícone em pixels.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- API de Streaming de Mídia do método Height
- API de Streaming de Mídia do método height, interface IDeviceIcon
- API de Streaming de Mídia da interface IDeviceIcon, método Height
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d813c572b0fc9e562d40326d830c5ef3530857601811df78c3acd541314b402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060286"
---
# <a name="ideviceiconheight-method"></a>Método IDeviceIcon::Height

Recupera a altura do ícone em pixels.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe um ponteiro para a altura do ícone em pixels.

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

 

