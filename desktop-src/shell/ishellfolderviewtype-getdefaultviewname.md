---
description: Obtém o nome da exibição padrão. Chame GetDisplayNameOf para recuperar os nomes das outras exibições.
title: Método IShellFolderViewType::GetDefaultViewName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 252616bd2391606b9942777caf07a2f5f58627a316f51e481c19fbfcc98599b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443266"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>Método IShellFolderViewType::GetDefaultViewName

Obtém o nome da exibição padrão. Chame [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar os nomes das outras exibições.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uFlags* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Sinalizadores opcionais; deve ser definido como 0.

</dd> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

O endereço de um ponteiro de cadeia de caracteres que recebe o nome de exibição padrão. A memória da cadeia de caracteres é alocada com [**SHStrDup.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




