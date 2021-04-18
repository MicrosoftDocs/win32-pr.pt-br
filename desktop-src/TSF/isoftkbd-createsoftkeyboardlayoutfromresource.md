---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeybboardLayoutFromResource cria um layout de teclado flexível a partir do recurso especificado.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardLayoutFromResource
- Método CreateSoftKeyboardLayoutFromResource de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810474"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>Método ISoftKbd:: CreateSoftKeyboardLayoutFromResource

O método **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** cria um layout de teclado flexível a partir do recurso especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszResFile* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que indica o nome do arquivo de recurso.

</dd> <dt>

*lpszResType* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que indica o tipo de recurso.

</dd> <dt>

*lpszXMLResString* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que identifica o recurso.

</dd> <dt>

*lpdwLayoutCookie* \[ fora\]
</dt> <dd>

Ponteiro para o buffer no qual esse método recupera um cookie de layout de teclado flexível.

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

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





