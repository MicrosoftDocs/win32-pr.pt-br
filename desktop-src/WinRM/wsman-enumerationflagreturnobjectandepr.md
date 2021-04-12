---
title: Método WSMan. EnumerationFlagReturnObjectAndEPR (WSManDisp. h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagReturnObjectAndEPR para uso no parâmetro flags de Session. Enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagReturnObjectAndEPR
- Método EnumerationFlagReturnObjectAndEPR Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagReturnObjectAndEPR
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
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455793"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a>Método WSMan. EnumerationFlagReturnObjectAndEPR

O método **EnumerationFlagReturnObjectAndEPR** retorna o valor do sinalizador de enumeração **EnumerationFlagReturnObjectAndEPR** para uso no parâmetro *flags* de [**Session. Enumerate**](session-enumerate.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**EnumerationFlagReturnObjectAndEPR** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**constantes de enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
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

 

 





