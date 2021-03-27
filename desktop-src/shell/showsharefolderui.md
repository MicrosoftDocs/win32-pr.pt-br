---
description: Exibe a guia compartilhamento de pasta na folha de propriedades da pasta especificada.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Função ShowShareFolderUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296934"
---
# <a name="showsharefolderui-function"></a>Função ShowShareFolderUI

Exibe a guia **compartilhamento de pasta** na folha de propriedades da pasta especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

Um identificador para a janela pai da folha de propriedades.

</dd> <dt>

*pszPath* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica o caminho para a pasta que exibe sua guia de **compartilhamento de pasta** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Essa função sempre retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo. lib associado. Você deve usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usá-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
