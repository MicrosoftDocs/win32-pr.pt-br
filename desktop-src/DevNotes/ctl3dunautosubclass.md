---
description: Desliga a subclasse automática.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Função Ctl3dUnAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ca7980705ca93ad88b7c9e535abe59c3cdcc2e011130c843f0e89a533ce97599
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654466"
---
# <a name="ctl3dunautosubclass-function"></a>Função Ctl3dUnAutoSubclass

Desliga a subclasse automática.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
