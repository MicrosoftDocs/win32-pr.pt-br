---
description: Inicia uma pesquisa para uma cadeia de caracteres de pesquisa especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Método IShellFolderSearchable:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647540"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Método IShellFolderSearchable:: FindString

Inicia uma pesquisa para uma cadeia de caracteres de pesquisa especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszTarget* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica a palavra-chave Search.

</dd> <dt>

*pdwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD \** _

Nenhum sinalizador está definido no momento; Defina como _ * NULL * *.

</dd> <dt>

*punkOnAsyncSearch* \[ no\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Um ponteiro para um objeto do tipo [_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown). Este objeto deve dar suporte à interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) . Defina como **NULL** se nenhum retorno de chamada for necessário.

</dd> <dt>

*ppidlOut* \[ fora\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Um ponteiro para uma estrutura de [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para a pasta de pesquisa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
