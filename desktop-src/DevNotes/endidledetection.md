---
description: Encerra o monitoramento de inatividade.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Função EndIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: a2ba6732b9221d4d4d43e670d0d42d39363d50dffc0d2d4b0daf378b10dd292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691406"
---
# <a name="endidledetection-function"></a>Função EndIdleDetection

\[Essa função não tem suporte e pode ser alterada ou não disponível no futuro. Em vez disso, use **a função GetLastInputInfo.**\]

Encerra o monitoramento de inatividade.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwReserved* 
</dt> <dd>

Esse parâmetro deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Essa função não é exportada por nome; especifique ordinal 4 ao chamar **GetProcAddress.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
