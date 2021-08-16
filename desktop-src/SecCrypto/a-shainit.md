---
description: Inicia o hash de um fluxo de dados.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Função A_SHAInit (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0081311988a5da0ae5ca21e924305918bb1e713a6cde3be1b77821c9b458cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774260"
---
# <a name="a_shainit-function"></a>Uma \_ função SHAInit

Inicia o hash de um fluxo de dados.

## <a name="syntax"></a>Sintaxe


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contexto* \[ do entrada, saída\]
</dt> <dd>

O contexto do SHA.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função é muito semelhante a SHAInit, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia. para obter mais informações, consulte [Windows provedores de NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
