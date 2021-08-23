---
description: Torna esse ponteiro para uma PIDL (lista de identificadores de item) uma parte inválida da pasta Shell.
title: Método IShellFolderSearchable::InvalidateSearch
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
ms.openlocfilehash: 5f443f3abd4a5cf2c1d0fc473c9267660d05c183a02c7f7705c1fabcbc9a8918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596566"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Método IShellFolderSearchable::InvalidateSearch

Torna esse ponteiro para uma PIDL (lista de identificadores de item) uma parte inválida da pasta Shell.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pidlSearch* \[ Em\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Um ponteiro para a [**estrutura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) da pasta de pesquisa.

</dd> <dt>

*pdwFlags* \[ Em\]
</dt> <dd>

Tipo: **DWORD \***

Nenhum sinalizador está definido no momento; definido como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Quando uma pasta de pesquisa é invalidada, ela pode executar a limpeza de todos os recursos que usou. O **método IShellFolderSearchable::InvalidateSearch** pode fazer com que uma pesquisa assíncrona seja cancelada e resultará na versão eventual do objeto de interface [**IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




