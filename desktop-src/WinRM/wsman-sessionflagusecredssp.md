---
title: Método WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Retorna o valor do sinalizador de autenticação WSManFlagUseCredSsp para uso no parâmetro flags do método WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método SessionFlagUseCredSsp
- Método SessionFlagUseCredSsp Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método SessionFlagUseCredSsp
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
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455195"
---
# <a name="wsmansessionflagusecredssp-method"></a>Método WSMan. SessionFlagUseCredSsp

Retorna o valor do sinalizador de autenticação **WSManFlagUseCredSsp** para uso no parâmetro *flags* do método [**WSMan. CreateSession**](wsman-createsession.md) . Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagUseCredSsp** é uma constante na enumeração **\_ \_ WSManSessionFlags** . Para obter mais informações, consulte [constantes de autenticação](authentication-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Redistribuível<br/>          | Windows Management Framework no Windows Server 2008 com SP2, Windows Vista com SP1 e Windows Vista com SP2<br/> |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>                                      |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





