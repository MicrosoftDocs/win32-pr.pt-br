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
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968255"
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

Digite: **HWND**

Um identificador para a janela pai da folha de propriedades.

</dd> <dt>

*pszPath* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica o caminho para a pasta que exibe sua guia de **compartilhamento de pasta** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Essa função sempre retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo. lib associado. Você deve usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usá-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
