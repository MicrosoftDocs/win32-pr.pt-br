---
title: Método WSMan.SessionFlagUseCredSsp (WSManDisp.h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseCredSsp para uso no parâmetro flags do método WSMan.CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseCredSsp Windows Gerenciamento Remoto
- Método SessionFlagUseCredSsp Windows Gerenciamento Remoto , objeto WSMan
- Objeto WSMan Windows Gerenciamento Remoto, Método SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642226"
---
# <a name="wsmansessionflagusecredssp-method"></a>Método WSMan.SessionFlagUseCredSsp

Retorna o valor do sinalizador de autenticação **WSManFlagUseCredSsp** para uso no parâmetro *flags* do [**método WSMan.CreateSession.**](wsman-createsession.md) Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**WSManFlagUseCredSsp** é uma constante na enumeração **\_ \_ WSManSessionFlags.** Para obter mais informações, consulte [Constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Redistribuível<br/>          | Windows Management Framework no Windows Server 2008 com SP2, Windows Vista com SP1 e Windows Vista com SP2<br/> |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>                                      |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sessão**](session.md)
</dt> </dl>

 

 





