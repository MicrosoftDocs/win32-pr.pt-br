---
description: Indica que uma pesquisa foi iniciada.
title: Método IShellFolderSearchableCallback::RunBegin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 026b5b458736a0805d48dc59715a1705ecdb8557037232332767946dd05d333d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223346"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a>Método IShellFolderSearchableCallback::RunBegin

Indica que uma pesquisa foi iniciada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwReserved* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Reservado. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Em resposta a esse retorno de chamada, o aplicativo pode habilitar **o botão** Cancelar, por exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




