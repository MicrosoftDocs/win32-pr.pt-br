---
title: Método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp.h)
description: Retorna o valor do sinalizador de enumeração EnumerationFlagHierarchyDeepBasePropsOnly para uso no parâmetro flags de Session.Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Método EnumerationFlagHierarchyDeepBasePropsOnly Windows Gerenciamento Remoto
- Método EnumerationFlagHierarchyDeepBasePropsOnly Windows Gerenciamento Remoto , objeto WSMan
- Método WSMan Windows Remote Management , EnumerationFlagHierarchyDeepBasePropsOnly
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
ms.openlocfilehash: 197c615b8d805fc142fa8afb2cf4fbb56ef22eec76caf63f03c27f3d9f131b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742454"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a>Método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly

O **método WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** retorna o valor do sinalizador de enumeração **EnumerationFlagHierarchyDeepBasePropsOnly** para uso no parâmetro *flags* [**de Session.Enumerate**](session-enumerate.md). Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [Constantes de sessão](session-constants.md).

**EnumerationFlagHierarchyDeepBasePropsOnly** é uma constante na enumeração **\_ WSManEnumFlags** e é descrita em [**Constantes de Enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
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

 

 





