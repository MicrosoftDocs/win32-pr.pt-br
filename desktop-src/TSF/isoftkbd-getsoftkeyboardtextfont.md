---
title: Método ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardTextFont recupera a fonte de texto usada por um teclado virtual.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardTextFont
- Método GetSoftKeyboardTextFont de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086079"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>Método ISoftKbd:: GetSoftKeyboardTextFont

O método **ISoftKbd:: GetSoftKeyboardTextFont** recupera a fonte de texto usada por um teclado virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLogFont* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera uma estrutura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define a fonte do texto para o teclado virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pLogFont* é inválido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

