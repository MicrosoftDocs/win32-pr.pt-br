---
title: Método WSMan.SessionFlagSkipCACheck (WSManDisp.h)
description: Retorna o valor do sinalizador de autenticação WSManFlagSkipCACheck para uso no parâmetro flags de WSMan.CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Método SessionFlagSkipCACheck Windows Gerenciamento Remoto
- Método SessionFlagSkipCACheck Windows gerenciamento remoto, objeto WSMan
- Objeto WSMan Windows Gerenciamento Remoto, Método SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe24e10ca7a568a6dc9b3af6efed6e31a3a9fde5acac70e2badab37d24373350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742025"
---
# <a name="wsmansessionflagskipcacheck-method"></a>Método WSMan.SessionFlagSkipCACheck

O **método WSMan.SessionFlagSkipCACheck** retorna o valor do sinalizador de autenticação **WSManFlagSkipCACheck** para uso no parâmetro *flags* [**de WSMan.CreateSession**](wsman-createsession.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método e exemplos de código, consulte [Constantes de sessão](session-constants.md).

**WSManFlagSkipCACheck** é uma constante na enumeração **\_ \_ WSManSessionFlags.** Para obter mais informações, consulte [**Constantes de autenticação**](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagSkipCACheck( _
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

 

 





