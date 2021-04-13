---
title: Método ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeyboardWindow cria uma janela de teclado suave.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardWindow
- Método CreateSoftKeyboardWindow de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499584"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>Método ISoftKbd:: CreateSoftKeyboardWindow

O método **ISoftKbd:: CreateSoftKeyboardWindow** cria uma janela de teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hOwner* \[ no\]
</dt> <dd>

Identificador da janela para conter o teclado virtual.

</dd> <dt>

*\_ Tipo de TitleBar* \[ em\]
</dt> <dd>

Tipo de barra de título da janela de teclado flexível. Os tipos possíveis são definidos pela enumeração de [**\_ tipo TITLEBAR**](titlebar-type.md) .

</dd> <dt>

*XPos* \[ no\]
</dt> <dd>

A posição x do canto superior esquerdo da janela de teclado suave.

</dd> <dt>

*YPos* \[ no\]
</dt> <dd>

A posição y do canto superior esquerdo da janela de teclado suave.

</dd> <dt>

*largura* \[ no\]
</dt> <dd>

A largura da janela de teclado flexível.

</dd> <dt>

*altura* \[ no\]
</dt> <dd>

A altura da janela de teclado suave.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros são inválidos.<br/> |



 

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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd::D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**tipo de TITLEBAR \_**](titlebar-type.md)
</dt> </dl>

 

 





