---
title: Método ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardTextFont define a fonte de texto usada por um teclado suave.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardTextFont
- Método SetSoftKeyboardTextFont de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813076"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>Método ISoftKbd:: SetSoftKeyboardTextFont

O método **ISoftKbd:: SetSoftKeyboardTextFont** define a fonte de texto usada por um teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLogFont* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define a fonte do texto para o teclado virtual.

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

[**ISoftKbd::GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

