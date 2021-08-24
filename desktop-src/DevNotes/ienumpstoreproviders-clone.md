---
description: Método IEnumPStoreProviders::Clone – cria outro enumerador que contém o mesmo estado de enumeração que o atual.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: Método IEnumPStoreProviders::Clone (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a88a814d5052dea51bade8046392ecfe7530d43e368b10700c614d42baafe398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542176"
---
# <a name="ienumpstoreprovidersclone-method"></a>Método IEnumPStoreProviders::Clone

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Cria outro enumerador que contém o mesmo estado de enumeração do atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppenum* \[ out\]
</dt> <dd>

Um ponteiro para um [**ponteiro IEnumPStoreProviders.**](ienumpstoreproviders.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
