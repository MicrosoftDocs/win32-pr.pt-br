---
description: Recupera um enumerador que retornará um ponteiro para uma PIDL (lista de identificadores de item) para cada exibição estendida.
title: 'Método IShellFolderViewType:: EnumViews'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988769"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>Método IShellFolderViewType:: EnumViews

Recupera um enumerador que retornará um ponteiro para uma PIDL (lista de identificadores de item) para cada exibição estendida.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*grfFlags* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Sinalizadores que indicam quais itens incluir na enumeração. Para obter uma lista de valores possíveis, consulte o tipo enumerado [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) . Esse parâmetro pode ser ignorado.

</dd> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

O endereço de uma variável de ponteiro do tipo [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) que recebe o enumerador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

As exibições são representadas para o usuário como pastas ocultas no diretório raiz (representado por PIDLs). Sempre que apropriado, a exibição padrão (fora da pasta raiz) é representada como **nulo**, ou vazia, PIDL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




