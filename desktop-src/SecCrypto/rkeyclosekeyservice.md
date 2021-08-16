---
description: Não há suporte para a função RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Função RKeyCloseKeyService (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5c7a075cf4869e350d90e278d009098cf4716d6518b1970c15b8b8264c93cd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900551"
---
# <a name="rkeyclosekeyservice-function"></a>Função RKeyCloseKeyService

Não há suporte para a função **RKeyCloseKeyService.**

**Windows Server 2003:** A **função RKeyCloseKeyService** fecha uma alça de serviço de chave aberta por uma chamada anterior para a [**função RKeyOpenKeyService.**](rkeyopenkeyservice.md) Observe que esse comportamento foi alterado com Windows Server 2003 com Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxe


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKeySvcCli* \[ Em\]
</dt> <dd>

Um [**handle KEYSVCC \_ HANDLE**](keysvcc-handle.md) aberto anteriormente por [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Esse valor não pode ser **NULL.**

</dd> <dt>

*pReserved* \[ in, out\]
</dt> <dd>

Reservado. De definir esse valor como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno será **um ULONG** que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




