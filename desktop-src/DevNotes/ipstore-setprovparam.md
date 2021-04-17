---
description: Define as informações do parâmetro especificado.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Método IPStore:: SetProvParam (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752371"
---
# <a name="ipstoresetprovparam-method"></a>Método IPStore:: SetProvParam

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Define as informações do parâmetro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ no\]
</dt> <dd>

Contém **o \_ \_ \_ \_ cache pw de liberação PP de PST** para liberar o cache de senha do usuário.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

O comprimento da senha no buffer.

</dd> <dt>

*pbData* 
</dt> <dd>

Um ponteiro para um buffer que contém a senha do usuário. Isso deve ser definido como **nulo**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** . Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
