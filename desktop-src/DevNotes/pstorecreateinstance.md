---
description: Recupera um ponteiro de interface para um provedor de armazenamento.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Função PStoreCreateInstance (Pstore.h)
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
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955685"
---
# <a name="pstorecreateinstance-function"></a>Função PStoreCreateInstance

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Essa função pode ser alterada ou não disponível em versões futuras do Windows. Use as **funções CryptProtectData** **e CryptUnprotectData** em vez dessa função.\]

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

*ppProvider* \[ out\]
</dt> <dd>

Um ponteiro para o ponteiro de interface recuperado para o provedor de armazenamento. Quando você terminar de usar a interface , decremente sua contagem de referência chamando seu [**método IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*pProviderID* \[ Em\]
</dt> <dd>

Um ponteiro para o **GUID** que identifica o provedor de armazenamento. Se esse parâmetro for **NULL,** o provedor de armazenamento base será usado.

</dd> <dt>

*pReserved* \[ Em\]
</dt> <dd>

Reservado; deve ser **NULL.**

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de **S \_ OK** indica que a função foi bem-sucedida.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação associada; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
