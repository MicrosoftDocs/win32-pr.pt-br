---
description: 'Método IEnumPStoreProviders:: Reset – redefine para o início da sequência de enumeração.'
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: 'Método IEnumPStoreProviders:: Reset (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a9214ace99021bebe9529cb8395aa217f8a8305d9ed0f42ab06998328d65f08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691296"
---
# <a name="ienumpstoreprovidersreset-method"></a>Método IEnumPStoreProviders:: Reset

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Redefine para o início da sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O valor de retorno é um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
