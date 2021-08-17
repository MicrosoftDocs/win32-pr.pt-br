---
description: Define a atribuição de Conjuntos de CPU padrão para threads no processo especificado. Threads criados, que não têm Conjuntos de CPU definidos explicitamente usando SetThreadSelectedCpuSets, herdarão os conjuntos especificados por SetProcessDefaultCpuSets automaticamente.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Função SetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793173"
---
# <a name="setprocessdefaultcpusets-function"></a>Função SetProcessDefaultCpuSets

Define a atribuição de Conjuntos de CPU padrão para threads no processo especificado. Threads criados, que não têm Conjuntos de CPU definidos explicitamente usando [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), herdarão os conjuntos especificados por **SetProcessDefaultCpuSets** automaticamente.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Processo* \[ Em\]
</dt> <dd>

Especifica o processo para o qual definir os Conjuntos de CPU padrão. Esse handle deve ter o direito de acesso PROCESS \_ SET \_ LIMITED \_ INFORMATION. O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*CpuSetIds* \[ in, opcional\]
</dt> <dd>

Especifica a lista de IDs do conjunto de CPU a ser definida como o conjunto de CPU padrão do processo. Se for NULL, **SetProcessDefaultCpuSets** limpará qualquer atribuição.

</dd> <dt>

*CpuSetIdCound* \[ Em\]
</dt> <dd>

Especifica o número de IDs na lista passada no **argumento CpuSetIds.** Se esse valor for NULL, isso deverá ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função não pode falhar quando os parâmetros válidos são passados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
