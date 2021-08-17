---
title: Método WSMan.EnumerationFlagReturnObject (WSManDisp.h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagReturnObject para uso no parâmetro flags de Session.Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnObject Windows Gerenciamento Remoto
- Método EnumerationFlagReturnObject Windows Gerenciamento Remoto , objeto WSMan
- O objeto WSMan Windows Gerenciamento Remoto, EnumerationFlagReturnObject
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72d070770cdfe23083dc588ab2111fe9d891d0b8462ee66fa930e2e2fea444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742255"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>Método WSMan.EnumerationFlagReturnObject

O **método WSMan.EnumerationFlagReturnObject** retorna o valor do sinalizador de **enumeração EnumerationFlagReturnObject** para uso no parâmetro *flags* [**de Session.Enumerate**](session-enumerate.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**EnumerationFlagReturnObject** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**Constantes de Enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagReturnObject( _
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

 

 





