---
title: Método WSMan.SessionFlagUseNoAuthentication (WSManDisp.h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseNoAuthentication para uso no parâmetro flags do método WSMan.CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseNoAuthentication Windows Gerenciamento Remoto
- Método SessionFlagUseNoAuthentication Windows Gerenciamento Remoto, objeto WSMan
- O objeto WSMan Windows Gerenciamento Remoto, Método SessionFlagUseNoAuthentication
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edb428a8c739c224e55bd4437dfdd6f544e9adf3039afb61df659b4969fb9ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412396"
---
# <a name="wsmansessionflagusenoauthentication-method"></a>Método WSMan.SessionFlagUseNoAuthentication

O **método WSMan.SessionFlagUseNoAuthentication** retorna o valor do sinalizador de autenticação **WSManFlagUseNoAuthentication** para uso no parâmetro *flags* do [**método WSMan.CreateSession.**](wsman-createsession.md) Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**WSManFlagUseNoAuthentication** é uma constante na enumeração **\_ \_ WSManSessionFlags.** Para obter mais informações, consulte //[Constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseNoAuthentication( _
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
| parâmetro<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sessão**](session.md)
</dt> </dl>

 

 





