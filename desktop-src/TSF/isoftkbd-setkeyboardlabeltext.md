---
title: Método ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: O método ISoftKbd SetKeyboardLabelText define o texto do rótulo do layout de um teclado virtual.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Estrutura de serviços de texto do método SetKeyboardLabelText
- Método SetKeyboardLabelText de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644972"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>Método ISoftKbd:: SetKeyboardLabelText

O método **ISoftKbd:: SetKeyboardLabelText** define o texto do rótulo do layout de um teclado virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKl* \[ no\]
</dt> <dd>

Identificador que é usado para recuperar o layout instalado para o teclado virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *hKl* é inválido.<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





