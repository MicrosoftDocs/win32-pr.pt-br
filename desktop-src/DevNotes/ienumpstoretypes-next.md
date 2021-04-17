---
description: Obtém o próximo número especificado de tipos de provedor na sequência de enumeração.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Método IEnumPStoreTypes:: Next (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747626"
---
# <a name="ienumpstoretypesnext-method"></a>Método IEnumPStoreTypes:: Next

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtém o próximo número especificado de tipos de provedor na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

O número de tipos de provedor solicitado.

</dd> <dt>

*rgelt* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres na qual retornar o nome do tipo de provedor.

</dd> <dt>

*pceltFetched* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o número de tipos de provedor realmente fornecidos.

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

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
