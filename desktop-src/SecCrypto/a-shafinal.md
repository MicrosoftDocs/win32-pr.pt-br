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
ms.openlocfilehash: 42a22cfca32409fdfa02586bb90c76f8e8f2489b22cfe2769b50d928d2564af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960285"
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

Essa função é muito semelhante a SHAFinal, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia. para obter mais informações, consulte [Windows provedores de NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
