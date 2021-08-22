---
description: A função GetDllVersion recupera o número de versão de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Função GetDllVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390706"
---
# <a name="getdllversion-function"></a>Função GetDllVersion

\[Essa função não tem mais suporte, portanto, seu comportamento não pode ser garantido. \]

A **função GetDllVersion** recupera o número de versão de Cabinet.dll.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O número de versão do arquivo (consulte [Recurso VERSIONINFO](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
