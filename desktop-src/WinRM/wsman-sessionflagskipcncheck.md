---
title: Método WSMan. SessionFlagSkipCNCheck (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagSkipCNCheck para uso no parâmetro flags de WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagSkipCNCheck
- método SessionFlagSkipCNCheck Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagSkipCNCheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339246d88dd7dc86e23b1a97442788fb969eb9de5a36f89c4ebadecd9f6e32ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613476"
---
# <a name="wsmansessionflagskipcncheck-method"></a>Método WSMan. SessionFlagSkipCNCheck

O método **WSMan. SessionFlagSkipCNCheck** retorna o valor do sinalizador de autenticação **WSManFlagSkipCNCheck** para uso no parâmetro *flags* de [**WSMan. CreateSession**](wsman-createsession.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagSkipCNCheck** é uma constante na enumeração **\_ \_ WSManSessionFlags** . Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de fora\]
</dt> <dd>

O valor da constante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

[**Sessão**](session.md)
</dt> </dl>

 

 





