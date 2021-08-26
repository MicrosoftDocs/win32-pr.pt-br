---
description: Método IEnumPStoreTypes::Reset – redefine para o início da sequência de enumeração.
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: Método IEnumPStoreTypes::Reset (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: dcb68cb73bb88a4bbe3225e37c9e72d17ca5385b403a8b41d9cfad84ffec81d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002086"
---
# <a name="ienumpstoretypesreset-method"></a>Método IEnumPStoreTypes::Reset

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Redefine para o início da sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
