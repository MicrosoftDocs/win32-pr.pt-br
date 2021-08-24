---
description: Lê as regras de acesso para um determinado tipo.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: Método IPStore::ReadAccessRuleSet (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d22f56c14df4d11a8979065ede81ab8418909033ffd816a233a18c51af7f66c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749746"
---
# <a name="ipstorereadaccessruleset-method"></a>Método IPStore::ReadAccessRuleSet

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Este método não está implementado.\]

Lê as regras de acesso para um determinado tipo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*pType* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*pSubtype* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*pInfo* \[ Em\]
</dt> <dd>

Reservado.

</dd> <dt>

*ppRules* \[ Em\]
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

 

 
