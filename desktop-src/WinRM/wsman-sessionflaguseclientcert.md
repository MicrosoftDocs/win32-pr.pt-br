---
title: Método WSMan.SessionFlagUseClientCertificate (WSManDisp.h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseClientCertificate para uso no parâmetro flags do método WSMan.CreateSession.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseClientCertificate Windows Gerenciamento Remoto
- Método SessionFlagUseClientCertificate Windows Gerenciamento Remoto , objeto WSMan
- Objeto WSMan Windows Gerenciamento Remoto, Método SessionFlagUseClientCertificate
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseClientCertificate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59220e3ead9e37579b354b82a97b8443ce8f66f93a7fffeff618c6563e7278d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997197"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a>Método WSMan.SessionFlagUseClientCertificate

O **método WSMan.SessionFlagUseClientCertificate** retorna o valor do sinalizador de autenticação **WSManFlagUseClientCertificate** para uso no parâmetro *flags* do [**método WSMan.CreateSession.**](wsman-createsession.md) Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**WSManFlagUseClientCertificate é** uma constante na enumeração **\_ \_ WSManAuthenticationFlags.** Para obter mais informações, consulte [Constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseClientCertificate( _
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

 

 





