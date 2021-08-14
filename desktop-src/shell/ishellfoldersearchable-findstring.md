---
description: Inicia uma pesquisa por uma cadeia de caracteres de pesquisa especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: Método IShellFolderSearchable::FindString (Mmc.h)
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
ms.openlocfilehash: 947cda4094491702fa0f847e6a8abd4fed7bcbe9bd3504c5f8aec2097b0d6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220932"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Método IShellFolderSearchable::FindString

Inicia uma pesquisa por uma cadeia de caracteres de pesquisa especificada.

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

*pwszTarget* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica a palavra-chave de pesquisa.

</dd> <dt>

*pdwFlags* \[ Em\]
</dt> <dd>

Tipo: **DWORD \***

Nenhum sinalizador está definido no momento; definido como **NULL.**

</dd> <dt>

*porqueOnAsyncSearch* \[ Em\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Um ponteiro para um objeto do tipo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Esse objeto deve dar suporte à interface [**IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md) Definido como **NULL** se nenhum retorno de chamada for necessário.

</dd> <dt>

*ppidlOut* \[ out\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Um ponteiro para uma [**estrutura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para a pasta de pesquisa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Mmc.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
