---
description: 'Método IEnumPStoreTypes:: Skip – ignora o próximo número especificado de itens na sequência de enumeração.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Método IEnumPStoreTypes:: Skip (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096734"
---
# <a name="ienumpstoretypesskip-method"></a>Método IEnumPStoreTypes:: Skip

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Ignora o próximo número especificado de itens na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

O número de tipos de provedor a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
