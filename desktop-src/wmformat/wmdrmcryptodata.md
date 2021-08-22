---
title: Estrutura WMDRMCryptoData (wmdrmsdk. h)
description: A estrutura WMDRMCryptoData contém informações sobre o algoritmo criptográfico usado para criptografar e descriptografar conteúdo.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Formato de mídia do Windows da estrutura WMDRMCryptoData
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083800"
---
# <a name="wmdrmcryptodata-structure"></a>Estrutura WMDRMCryptoData

A estrutura **WMDRMCryptoData** contém informações sobre o algoritmo criptográfico usado para criptografar e descriptografar conteúdo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**cryptotype**
</dt> <dd>

Membro da enumeração [**do \_ \_ tipo de criptografia DRM**](drm-crypto-type.md) especificando o tipo de algoritmo criptográfico.

</dd> <dt>

**qwCounterID**
</dt> <dd>

Os bits de 64 altos do modo de contador AES de 128 bits. Esse membro só será usado se o membro **cryptotype** estiver definido como **crypto \_ Type \_ MCE**.

</dd> <dt>

**qwOffset**
</dt> <dd>

Os poucos 64 bits do modo de contador AES de 128 bits. Esse membro só será usado se o membro **cryptotype** estiver definido como **crypto \_ Type \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





