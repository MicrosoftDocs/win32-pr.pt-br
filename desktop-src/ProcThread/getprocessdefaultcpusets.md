---
description: Recupera a lista de Conjuntos de CPU no conjunto padrão de processo que foi definido por SetProcessDefaultCpuSets. Se nenhum Conjunto de CPU padrão for definido para um determinado processo, RequiredIdCount será definido como 0 e a função terá êxito.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Função GetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3c5d71e4811411756719177647fda8dd76224f756629ad01794720d291565b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886696"
---
# <a name="getprocessdefaultcpusets-function"></a>Função GetProcessDefaultCpuSets

Recupera a lista de Conjuntos de CPU no conjunto padrão de processo que foi definido por [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md). Se nenhum Conjunto de CPU padrão for definido para um determinado processo, **RequiredIdCount** será definido como 0 e a função terá êxito.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Processo* \[ Em\]
</dt> <dd>

Especifica um handle de processo para o processo a ser consultado. Esse handle deve ter o direito de acesso PROCESS \_ QUERY \_ LIMITED \_ INFORMATION. O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*CpuSetIds* \[ out, opcional\]
</dt> <dd>

Especifica um buffer opcional para recuperar a lista de identificadores do Conjunto de CPU.

</dd> <dt>

*CpuSetIdCount* \[ Em\]
</dt> <dd>

Especifica a capacidade do buffer especificada em **CpuSetIds.** Se o buffer for NULL, ele deverá ser 0.

</dd> <dt>

*RequiredIdCount* \[ out\]
</dt> <dd>

Especifica a capacidade necessária do buffer para manter toda a lista de Conjuntos de CPU padrão do processo. No retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa API retorna TRUE em caso de êxito. Se o buffer não for grande o suficiente, a API retornará FALSE e o **valor GetLastError** será ERROR \_ INSUFFICIENT \_ BUFFER. Essa API não pode falhar quando os parâmetros válidos são passados e o buffer de retorno é grande o suficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

