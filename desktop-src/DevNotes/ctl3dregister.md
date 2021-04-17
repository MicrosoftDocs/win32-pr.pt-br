---
description: Registra um aplicativo como um cliente do CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Função Ctl3dRegister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748928"
---
# <a name="ctl3dregister-function"></a>Função Ctl3dRegister

Registra um aplicativo como um cliente do CTL3D.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Um identificador para o aplicativo a ser registrado como um cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se os efeitos 3D estiverem ativos; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Um aplicativo que usa CTL3D deve chamar essa função em WinMain.

os efeitos 3D não estão disponíveis em sistemas com resolução inferior a VGA.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
