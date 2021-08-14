---
description: Grava as regras de acesso para o tipo fornecido.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'Método IPStore:: WriteAccessRuleset (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955895"
---
# <a name="ipstorewriteaccessruleset-method"></a>Método IPStore:: WriteAccessRuleset

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Este método não está implementado.\]

Grava as regras de acesso para o tipo fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*pType* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*pSubtype* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*pInfo* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*pRules* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 
