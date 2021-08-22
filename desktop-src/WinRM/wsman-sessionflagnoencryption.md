---
title: Método WSMan. SessionFlagNoEncryption (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagNoEncryption para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagNoEncryption
- método SessionFlagNoEncryption Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagNoEncryption
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22b1f3e278a5deafc890ee8aacf21e36174255dac82fc123647e890323a34b28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613496"
---
# <a name="wsmansessionflagnoencryption-method"></a>Método WSMan. SessionFlagNoEncryption

O método **WSMan. SessionFlagNoEncryption** retorna o valor do sinalizador de autenticação **WSManFlagNoEncryption** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) . Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagNoEncryption** é uma constante na enumeração **\_ \_ WSManSessionFlags** . Para obter mais informações, consulte [outras constantes de sessão](other-session-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagNoEncryption( _
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

 

 





