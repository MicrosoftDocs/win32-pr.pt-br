---
title: Método WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Retorna o valor da constante de enumeração WSManFlagNonXmlText para uso no parâmetro flags do método Session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método EnumerationFlagNonXmlText
- método EnumerationFlagNonXmlText Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742285"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>Método WSMan. EnumerationFlagNonXmlText

O **WSMan. EnumerationFlagNonXmlText** retorna o valor da constante de enumeração **WSManFlagNonXmlText** para uso no parâmetro *flags* do método [**Session. Enumerate**](session-enumerate.md) . Esse método fornece uma sintaxe mais eficiente para usar a constante para que os scripts não sejam necessários para definir um valor constante. Para obter mais informações sobre como chamar esse método, consulte [constantes de sessão](session-constants.md).

**WSManFlagNonXmlText** é uma constante na enumeração **\_ \_ WSManEnumFlags** . Para obter mais informações, consulte [**constantes de enumeração**](enumeration-constants.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.EnumerationFlagNonXmlText( _
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

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





