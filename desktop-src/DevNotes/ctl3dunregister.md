---
description: Cancela o registro de um aplicativo como um cliente do CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Função Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748517"
---
# <a name="ctl3dunregister-function"></a>Função Ctl3dUnregister

Cancela o registro de um aplicativo como um cliente do CTL3D.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Um identificador para o aplicativo ter o registro cancelado como um cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o aplicativo tiver o registro cancelado como um cliente de CTL3D; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Um aplicativo que usa CTL3D deve chamar essa função em WinMain.

os efeitos 3D não estão disponíveis em sistemas com resolução inferior a VGA.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
