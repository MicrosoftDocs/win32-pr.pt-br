---
description: Inicia o processo de cancelar uma pesquisa assíncrona pendente.
title: 'Método IShellFolderSearchable:: CancelAsyncSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967501"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>Método IShellFolderSearchable:: CancelAsyncSearch

Inicia o processo de cancelar uma pesquisa assíncrona pendente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pidlSearch* \[ no\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Um ponteiro para uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para a pesquisa.

</dd> <dt>

*pdwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD \** _

Nenhum sinalizador está definido no momento; Defina como _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Retorna S \_ OK se cancelar, ou S \_ false se a pesquisa não estiver em execução.

## <a name="remarks"></a>Comentários

Quando a pesquisa for realmente cancelada, [**RunEnd**](ishellfoldersearchablecallback-runend.md) será chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




