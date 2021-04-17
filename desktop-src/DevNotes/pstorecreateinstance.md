---
description: Recupera um ponteiro de interface para um provedor de armazenamento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Função PStoreCreateInstance (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752567"
---
# <a name="pstorecreateinstance-function"></a>Função PStoreCreateInstance

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Essa função pode ser alterada ou indisponível em versões futuras do Windows. Use as funções **CryptProtectData** e **CryptUnprotectData** em vez dessa função.\]

Recupera um ponteiro de interface para um provedor de armazenamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppProvider* \[ fora\]
</dt> <dd>

Um ponteiro para o ponteiro de interface recuperado para o provedor de armazenamento. Quando você terminar de usar a interface, decrementará sua contagem de referência chamando seu método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Este parâmetro não pode ser **nulo**.

</dd> <dt>

*pProviderID* \[ no\]
</dt> <dd>

Um ponteiro para o **GUID** que identifica o provedor de armazenamento. Se esse parâmetro for **nulo**, o provedor de armazenamento base será usado.

</dd> <dt>

*preservado* \[ no\]
</dt> <dd>

Reservado deve ser **NULL**.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de **S \_ OK** indica que a função foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
