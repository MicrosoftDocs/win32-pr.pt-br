---
description: Anuidade o registro de um aplicativo como um cliente de CTL3D.
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
ms.openlocfilehash: 32a954efceba7400692ad92c91bedb47283587827739c19f23e7802e1481fbe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691496"
---
# <a name="ctl3dunregister-function"></a>Função Ctl3dUnregister

Anuidade o registro de um aplicativo como um cliente de CTL3D.

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

Um lidar com o aplicativo a ser não registro como um cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o aplicativo não tiver o registro como um cliente de CTL3D; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Um aplicativo que usa CTL3D deve chamar essa função no WinMain.

Os efeitos 3D não estão disponíveis em sistemas que têm menos de resolução de VGA.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
