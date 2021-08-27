---
description: Destina-se a definir as informações de parâmetro especificadas.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: Método IPStore::GetProvParam (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955905"
---
# <a name="ipstoregetprovparam-method"></a>Método IPStore::GetProvParam

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Este método não está implementado.\]

Destina-se a definir as informações de parâmetro especificadas. Observe, no entanto, que ele não é implementado e sempre falhará.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*pcbData* \[ out\]
</dt> <dd>

Reservado.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Reservado.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

As chamadas para esse método sempre falharão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
