---
description: Adiciona dados a um objeto de hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate função (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 103438e3ef0747aa6170848398621b0246bd15366be4d1171ce5735942011007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101066"
---
# <a name="a_shaupdate-function"></a>Uma \_ função SHAUpdate

Adiciona dados a um objeto de hash especificado.

## <a name="syntax"></a>Sintaxe


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contexto* \[ in, out\]
</dt> <dd>

O contexto SHA.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

A tabela de hash.

</dd> <dt>

*BufferSize* 
</dt> <dd>

O tamanho do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função pode ser chamada várias vezes para calcular o hash em fluxos de dados longos ou fluxos de dados descontinuados. A [**função \_ A SHAFinal**](a-shafinal.md) deve ser chamada antes de recuperar o valor de hash.

Essa função é muito semelhante a SHAUpdate, mas é chamada diretamente da biblioteca, em vez de ser roteada por meio da infraestrutura de criptografia. Para obter mais informações, [consulte Windows provedores NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
