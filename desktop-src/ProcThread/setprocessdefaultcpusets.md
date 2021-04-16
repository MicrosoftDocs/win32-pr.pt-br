---
description: Define a atribuição de conjuntos de CPU padrão para threads no processo especificado. Os threads criados, que não têm conjuntos de CPU definidos explicitamente usando SetThreadSelectedCpuSets, herdarão os conjuntos especificados por SetProcessDefaultCpuSets automaticamente.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Função SetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757742"
---
# <a name="setprocessdefaultcpusets-function"></a>Função SetProcessDefaultCpuSets

Define a atribuição de conjuntos de CPU padrão para threads no processo especificado. Os threads criados, que não têm conjuntos de CPU definidos explicitamente usando [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), herdarão os conjuntos especificados por **SetProcessDefaultCpuSets** automaticamente.

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

*Processo* \[ do no\]
</dt> <dd>

Especifica o processo para o qual definir os conjuntos de CPU padrão. Esse identificador deve ter o \_ direito de \_ acesso definir informações limitadas \_ do processo. O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*CpuSetIds* \[ em, opcional\]
</dt> <dd>

Especifica a lista de IDs de conjunto de CPU a ser definida como o conjunto de CPU padrão do processo. Se isso for nulo, o **SetProcessDefaultCpuSets** desmarcará qualquer atribuição.

</dd> <dt>

*CpuSetIdCound* \[ no\]
</dt> <dd>

Especifica o número de IDs na lista passada no argumento **CpuSetIds** . Se esse valor for nulo, ele deverá ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não pode falhar quando passaram parâmetros válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
