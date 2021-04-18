---
description: Computa o hash final dos dados inseridos pela função MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Função A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756158"
---
# <a name="a_shafinal-function"></a>Uma \_ função SHAFinal

Computa o hash final dos dados inseridos pela função MD5Update.

## <a name="syntax"></a>Sintaxe


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contexto* \[ do entrada, saída\]
</dt> <dd>

O contexto do SHA.

</dd> <dt>

*Resultado* \[ fora\]
</dt> <dd>

A tabela de hash resultante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função é muito semelhante a SHAFinal, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia. Para obter mais informações, consulte [provedores do Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
