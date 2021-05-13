---
description: Torna esse ponteiro para uma lista de identificadores de item (PIDL) uma parte inválida da pasta do Shell.
title: 'Método IShellFolderSearchable:: InvalidateSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841687"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Método IShellFolderSearchable:: InvalidateSearch

Torna esse ponteiro para uma lista de identificadores de item (PIDL) uma parte inválida da pasta do Shell.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pidlSearch* \[ no\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Um ponteiro para a estrutura de [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) da pasta de pesquisa.

</dd> <dt>

*pdwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD \***

Nenhum sinalizador está definido no momento; Defina como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando uma pasta de pesquisa é invalidada, ela pode executar a limpeza de todos os recursos que ele usou. O método **IShellFolderSearchable:: InvalidateSearch** pode fazer com que uma pesquisa assíncrona seja cancelada e resultará na versão eventual do objeto de interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




