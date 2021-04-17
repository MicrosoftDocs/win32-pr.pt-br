---
description: Destinado a definir as informações do parâmetro especificado.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Método IPStore:: GetProvParam (Pstore. h)'
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
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747904"
---
# <a name="ipstoregetprovparam-method"></a>Método IPStore:: GetProvParam

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Este método não está implementado.\]

Destinado a definir as informações do parâmetro especificado. Observe, no entanto, que ele não está implementado e sempre falhará.

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

*dwParam* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*pcbData* \[ fora\]
</dt> <dd>

Reservado.

</dd> <dt>

*ppbData* \[ fora\]
</dt> <dd>

Reservado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

As chamadas para esse método sempre falharão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
