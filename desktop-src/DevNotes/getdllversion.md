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
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754787"
---
# <a name="getdllversion-function"></a>Função GetDllVersion

\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido. \]

A função **GetDllVersion** recupera o número de versão de Cabinet.dll.

## <a name="syntax"></a>Sintaxe


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O número de versão do arquivo (consulte o [recurso VERSIONINFO](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
