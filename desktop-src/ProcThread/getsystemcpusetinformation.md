---
description: Permite que um aplicativo consulte os conjuntos de CPU disponíveis no sistema e seu estado atual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Função GetSystemCpuSetInformation (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169505"
---
# <a name="getsystemcpusetinformation-function"></a>Função GetSystemCpuSetInformation

Permite que um aplicativo consulte os conjuntos de CPU disponíveis no sistema e seu estado atual.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Informações* \[ do out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de informações do conjunto de CPU do sistema que recebe os dados do conjunto de CPU. [**\_ \_ \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) Passe NULL com um comprimento de buffer de 0 para determinar o tamanho de buffer necessário.

</dd> <dt>

*BufferLength* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer de saída passado como o argumento de informações.

</dd> <dt>

*ReturnedLength* \[ fora\]
</dt> <dd>

O comprimento, em bytes, dos dados válidos no buffer de saída se o buffer for grande o suficiente ou o tamanho necessário do buffer de saída. Se não houver nenhum conjunto de CPU, esse valor será 0.

</dd> <dt>

*Processo* \[ do em, opcional\]
</dt> <dd>

Um identificador opcional para um processo. Esse processo é usado para determinar o valor do sinalizador **AllocatedToTargetProcess** na estrutura de informações do conjunto de CPU do sistema \_ \_ \_ . Se um conjunto de CPU for alocado para o processo especificado, o sinalizador será definido. Caso contrário, fica claro. Esse identificador deve ter o \_ direito de \_ acesso de informações limitado à consulta de processo \_ . O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Reservado, deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a API for realizada com sucesso, ela retornará TRUE. Se falhar, o motivo do erro estará disponível por meio de **GetLastError**. Se o buffer de informações era nulo ou não é grande o suficiente, o buffer de erro de código de erro \_ insuficiente \_ é retornado. Essa API não pode falhar quando passou parâmetros válidos e um buffer que é grande o suficiente para conter todos os dados de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

