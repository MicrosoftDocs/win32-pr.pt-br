---
title: Método WSMan.SessionFlagUseKerberos (WSManDisp.h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseKerberos para uso no parâmetro flags de WSMan.CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseKerberos Windows Gerenciamento Remoto
- Método SessionFlagUseKerberos Windows gerenciamento remoto, objeto WSMan
- O objeto WSMan Windows Gerenciamento Remoto, Método SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468d6096343e3c0fe67369abe3927870f2e1eaf89a2d12b9c73e3560d436859e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997196"
---
# <a name="wsmansessionflagusekerberos-method"></a>Método WSMan.SessionFlagUseKerberos

O **método WSMan.SessionFlagUseKerberos** retorna o valor do sinalizador de autenticação **WSManFlagUseKerberos** para uso no parâmetro *flags* [**de WSMan.CreateSession**](wsman-createsession.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**WSManFlagUseKerberos** é uma constante na enumeração **\_ \_ WSManSessionFlags.** Para obter mais informações, consulte [Constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ out\]
</dt> <dd>

O valor da constante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sessão**](session.md)
</dt> </dl>

 

 





