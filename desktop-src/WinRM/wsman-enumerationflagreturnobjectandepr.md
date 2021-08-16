---
title: Método WSMan.EnumerationFlagReturnObjectAndEPR (WSManDisp.h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagReturnObjectAndEPR para uso no parâmetro flags de Session.Enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagReturnObjectAndEPR Windows Gerenciamento Remoto
- Método EnumerationFlagReturnObjectAndEPR Windows Gerenciamento Remoto , objeto WSMan
- O objeto WSMan Windows Gerenciamento Remoto, EnumerationFlagReturnObjectAndEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa63e84770010a05e144c702a10a814aea4cf8323681f6e95c8bf2facc1dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742275"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a>Método WSMan.EnumerationFlagReturnObjectAndEPR

O **método EnumerationFlagReturnObjectAndEPR** retorna o valor do sinalizador de enumeração **EnumerationFlagReturnObjectAndEPR** para uso no parâmetro *flags* [**de Session.Enumerate**](session-enumerate.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**EnumerationFlagReturnObjectAndEPR** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**Constantes de Enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
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

 

 





