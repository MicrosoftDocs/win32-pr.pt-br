---
description: Adiciona dados a um objeto hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Função A_SHAUpdate (SHA. h)
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
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762026"
---
# <a name="a_shaupdate-function"></a>Uma \_ função SHAUpdate

Adiciona dados a um objeto hash especificado.

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

*Contexto* \[ do entrada, saída\]
</dt> <dd>

O contexto do SHA.

</dd> <dt>

*Buffer* \[ fora\]
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

Essa função pode ser chamada várias vezes para computar o hash em fluxos de dados longos ou fluxos de dados descontínuos. A [**função \_ SHAFinal**](a-shafinal.md) deve ser chamada antes da recuperação do valor de hash.

Essa função é muito semelhante a SHAUpdate, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia. Para obter mais informações, consulte [provedores do Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
