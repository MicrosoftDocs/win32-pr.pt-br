---
description: Reconstrói um ponteiro para uma PIDL (lista de identificadores de item) de uma representação hierárquica da pasta do Shell em uma representação diferente.
title: 'Método IShellFolderViewType:: TranslateViewPidl'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502075"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>Método IShellFolderViewType:: TranslateViewPidl

Reconstrói um ponteiro para uma PIDL (lista de identificadores de item) de uma representação hierárquica da pasta do Shell em uma representação diferente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ no\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

A matriz de IDs de item relativa à pasta raiz.

</dd> <dt>

*pidlView* \[ no\]
</dt> <dd>

Tipo: **PCUIDLIST \_ relativo**

PIDL especial da exibição.

</dd> <dt>

*ppidlOut* \[ no\]
</dt> <dd>

Tipo: **PCUIDLIST \_ Relative \** _

O endereço de uma variável PIDL para receber a tradução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando terminar, você deverá liberar o PIDL retornado com [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




