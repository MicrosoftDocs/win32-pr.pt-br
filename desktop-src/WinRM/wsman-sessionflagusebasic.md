---
title: Método WSMan. SessionFlagUseBasic (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseBasic para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseBasic
- Método SessionFlagUseBasic Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseBasic
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009016"
---
# <a name="wsmansessionflagusebasic-method"></a>Método WSMan. SessionFlagUseBasic

O método **WSMan. SessionFlagUseBasic** retorna o valor do sinalizador de autenticação **WSManFlagUseBasic** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) . Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagUseBasic** é uma constante na enumeração **\_ \_ WSManSessionFlags** . Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseBasic( _
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

 

 





