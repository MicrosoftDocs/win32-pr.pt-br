---
title: Método ISoftKbd SetKeyboardLabelText (Softkbdc.h)
description: O método ISoftKbd SetKeyboardLabelText define o texto do rótulo do layout para um teclado soft.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Método SetKeyboardLabelText Estrutura de Serviços de Texto
- Método SetKeyboardLabelText Estrutura de Serviços de Texto interface , ISoftKbd
- Interface ISoftKbd Estrutura de Serviços de Texto , método SetKeyboardLabelText
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
ms.openlocfilehash: d15e81e2ff29affaa6bf6e87f87410d9c9d3ef7e913998a1bffa1ab6b0dff3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877411"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>Método ISoftKbd::SetKeyboardLabelText

O **método ISoftKbd::SetKeyboardLabelText** define o texto do rótulo do layout para um teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKl* \[ Em\]
</dt> <dd>

O handle usado para recuperar o layout instalado para o teclado suave.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro hKl* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





