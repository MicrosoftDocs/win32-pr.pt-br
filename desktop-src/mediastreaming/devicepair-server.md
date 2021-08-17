---
title: Propriedade do servidor DevicePair (Asptlb. h)
description: Obtém o servidor para o par de dispositivo básico ativo.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API de streaming de mídia de propriedade de servidor
- API de streaming de mídia de propriedade de servidor, interface DevicePair
- API de streaming de mídia da interface DevicePair, Propriedade do servidor
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100720"
---
# <a name="devicepairserver-property"></a>Propriedade DevicePair:: Server

Obtém o servidor para o par de dispositivo básico ativo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valor da propriedade

Recebe um objeto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa o dispositivo de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Asptlb. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

