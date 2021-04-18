---
description: Recupera a lista de conjuntos de CPU no conjunto padrão de processo que foi definido por SetProcessDefaultCpuSets. Se nenhum conjunto de CPU padrão for definido para um determinado processo, o RequiredIdCount será definido como 0 e a função terá sucesso.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Função GetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766360"
---
# <a name="getprocessdefaultcpusets-function"></a>Função GetProcessDefaultCpuSets

Recupera a lista de conjuntos de CPU no conjunto padrão de processo que foi definido por [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md). Se nenhum conjunto de CPU padrão for definido para um determinado processo, o **RequiredIdCount** será definido como 0 e a função terá sucesso.

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

*Processo* \[ do no\]
</dt> <dd>

Especifica um identificador de processo para o processo a ser consultado. Esse identificador deve ter o \_ direito de \_ acesso de informações limitado à consulta de processo \_ . O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*CpuSetIds* \[ out, opcional\]
</dt> <dd>

Especifica um buffer opcional para recuperar a lista de identificadores de conjunto de CPU.

</dd> <dt>

*CpuSetIdCount* \[ no\]
</dt> <dd>

Especifica a capacidade do buffer especificado em **CpuSetIds**. Se o buffer for nulo, ele deverá ser 0.

</dd> <dt>

*RequiredIdCount* \[ fora\]
</dt> <dd>

Especifica a capacidade necessária do buffer para manter a lista completa de conjuntos de CPU de processo padrão. Após o retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa API retorna TRUE em caso de êxito. Se o buffer não for grande o suficiente, a API retornará FALSE e o valor **GetLastError** será um \_ buffer insuficiente de erro \_ . Esta API não pode falhar quando passou parâmetros válidos e o buffer de retorno é grande o suficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

