---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile cria um layout de teclado flexível a partir do arquivo XML especificado.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardLayoutFromXMLFile
- Método CreateSoftKeyboardLayoutFromXMLFile de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811021"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>Método ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile

O método **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** cria um layout de teclado flexível a partir do arquivo XML especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszKeyboardDesFile* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que indica o nome do arquivo XML.

</dd> <dt>

*szFileStrLen* \[ no\]
</dt> <dd>

Cadeia de caracteres terminada em zero indicando o comprimento do arquivo XML.

</dd> <dt>

*pdwLayoutCookie* \[ fora\]
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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





