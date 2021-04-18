---
title: Método WSMan. EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp. h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagHierarchyDeepBasePropsOnly para uso no parâmetro flags de Session. Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagHierarchyDeepBasePropsOnly
- Método EnumerationFlagHierarchyDeepBasePropsOnly Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagHierarchyDeepBasePropsOnly
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a0ed7d725f60e673d3426be1b11179ec8333d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791273"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a>Método WSMan. EnumerationFlagHierarchyDeepBasePropsOnly

O método **WSMan. EnumerationFlagHierarchyDeepBasePropsOnly** retorna o valor do sinalizador de enumeração **EnumerationFlagHierarchyDeepBasePropsOnly** para uso no parâmetro *flags* de [**Session. Enumerate**](session-enumerate.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**EnumerationFlagHierarchyDeepBasePropsOnly** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**constantes de enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
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

 

 





