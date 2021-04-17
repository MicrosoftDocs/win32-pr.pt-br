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
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811247"
---
# <a name="ipstorewriteaccessruleset-method"></a>Método IPStore:: WriteAccessRuleset

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

 

 
