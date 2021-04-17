---
description: Cria outro enumerador que contém o mesmo estado de enumeração do atual.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Método IEnumPStoreItems:: clone (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755633"
---
# <a name="ienumpstoreitemsclone-method"></a>Método IEnumPStoreItems:: clone

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Cria outro enumerador que contém o mesmo estado de enumeração do atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro [**IEnumPStoreItems**](ienumpstoreitems.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
