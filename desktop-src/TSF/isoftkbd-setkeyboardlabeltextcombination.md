---
title: Método ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: O método ISoftKbd SetKeyboardLabelTextCombination define uma combinação de rótulo e texto usado para descrever um teclado suave.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Estrutura de serviços de texto do método SetKeyboardLabelTextCombination
- Método SetKeyboardLabelTextCombination de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810473"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>Método ISoftKbd:: SetKeyboardLabelTextCombination

O método **ISoftKbd:: SetKeyboardLabelTextCombination** define uma combinação de rótulo e texto usado para descrever um teclado virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nModifierCombination* \[ no\]
</dt> <dd>

Combinação de rótulo e texto usado para descrever o teclado virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *nModifierCombination* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





