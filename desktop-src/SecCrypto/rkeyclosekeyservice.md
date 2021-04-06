---
description: Não há suporte para a função RKeyCloseKeyService.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Função RKeyCloseKeyService (Rkeysvcc. h)
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
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827141"
---
# <a name="rkeyclosekeyservice-function"></a>Função RKeyCloseKeyService

Não há suporte para a função **RKeyCloseKeyService** .

**Windows Server 2003:** A função **RKeyCloseKeyService** fecha um identificador de serviço de chave aberto por uma chamada anterior à função [**RKeyOpenKeyService**](rkeyopenkeyservice.md) . Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxe


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKeySvcCli* \[ no\]
</dt> <dd>

Um identificador de [**\_ identificador KEYSVCC**](keysvcc-handle.md) aberto anteriormente pelo [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Esse valor não pode ser **nulo**.

</dd> <dt>

*preservado* \[ entrada, saída\]
</dt> <dd>

Reservado. Defina esse valor como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




