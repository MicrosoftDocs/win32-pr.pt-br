---
title: Método WSMan. SessionFlagUseClientCertificate (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseClientCertificate para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseClientCertificate
- Método SessionFlagUseClientCertificate Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseClientCertificate
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
ms.openlocfilehash: cbbcbc1a920cbd7ce2b58e29c52fc08245b8aa35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294756"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a>Método WSMan. SessionFlagUseClientCertificate

O método **WSMan. SessionFlagUseClientCertificate** retorna o valor do sinalizador de autenticação **WSManFlagUseClientCertificate** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) . Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagUseClientCertificate** é uma constante na enumeração **\_ \_ WSManAuthenticationFlags** . Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseClientCertificate( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de fora\]
</dt> <dd>

O valor da constante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





