---
title: Método WSMan. createconnectoptions (WSManDisp. h)
description: Cria um objeto ConnectionOptions que especifica o nome de usuário e a senha usados ao criar uma sessão.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- método createconnectoptions Gerenciamento Remoto do Windows
- método createconnectoptions Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método createconnectoptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742663"
---
# <a name="wsmancreateconnectionoptions-method"></a>Método WSMan. createconnectoptions

Cria um objeto [**ConnectionOptions**](connectionoptions.md) que especifica o nome de usuário e a senha usados ao criar uma sessão.

## <a name="syntax"></a>Sintaxe


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Um objeto [**ConnectionOptions**](connectionoptions.md) usado para especificar um par de nome de usuário e senha que é usado para identificar um usuário para autenticação.

## <a name="remarks"></a>Comentários

A sintaxe a seguir é usada para chamar esse método.


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





