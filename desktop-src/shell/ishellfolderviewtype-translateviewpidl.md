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
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842667"
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

Tipo: **PCUIDLIST \_ relativo \***

O endereço de uma variável PIDL para receber a tradução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando terminar, você deverá liberar o PIDL retornado com [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




