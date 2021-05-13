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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842987"
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

Tipo: **DWORD \***

Nenhum sinalizador está definido no momento; Defina como **nulo**.

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



 

 




