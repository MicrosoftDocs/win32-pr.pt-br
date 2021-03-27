---
description: Obtém o nome da exibição padrão. Chame GetDisplayNameOf para recuperar os nomes das outras exibições.
title: 'Método IShellFolderViewType:: getmodopadrãoname'
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
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967497"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a>Método IShellFolderViewType:: getmodopadrãoname

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

*uFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Sinalizadores opcionais; deve ser definido como 0.

</dd> <dt>

*ppwszName* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR \** _

O endereço de um ponteiro de cadeia de caracteres que recebe o nome de exibição padrão. A memória da cadeia de caracteres é alocada com [_ *SHStrDup* *](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




