---
description: Permite que um aplicativo consulte os Conjuntos de CPU disponíveis no sistema e seu estado atual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Função GetSystemCpuSetInformation (Processthreadapi.h)
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
ms.openlocfilehash: 011a809c78f2e94e6d16bbe5deb716ee7e97db356765bb771709048d3b00d05a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995366"
---
# <a name="getsystemcpusetinformation-function"></a>Função GetSystemCpuSetInformation

Permite que um aplicativo consulte os Conjuntos de CPU disponíveis no sistema e seu estado atual.

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

*Informações* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [**\_ SYSTEM CPU SET \_ \_ INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) que recebe os dados do Conjunto de CPU. Passe NULL com um comprimento de buffer de 0 para determinar o tamanho do buffer necessário.

</dd> <dt>

*BufferLength* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do buffer de saída passado como o argumento Information.

</dd> <dt>

*ReturnedLength* \[ out\]
</dt> <dd>

O comprimento, em bytes, dos dados válidos no buffer de saída se o buffer for grande o suficiente ou o tamanho necessário do buffer de saída. Se nenhum Conjunto de CPU existir, esse valor será 0.

</dd> <dt>

*Processo* \[ in, opcional\]
</dt> <dd>

Um alça opcional para um processo. Esse processo é usado para determinar o valor do sinalizador **AllocatedToTargetProcess** na estrutura SYSTEM \_ CPU SET \_ \_ INFORMATION. Se um Conjunto de CPU for alocado ao processo especificado, o sinalizador será definido. Caso contrário, fica claro. Esse handle deve ter o direito de acesso PROCESS \_ QUERY \_ LIMITED \_ INFORMATION. O valor retornado por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) também pode ser especificado aqui.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Reservado, deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a API for bem-sucedida, ela retornará TRUE. Se falhar, o motivo do erro estará disponível por meio **de GetLastError.** Se o buffer de informações for NULL ou não for grande o suficiente, o código de erro ERROR \_ INSUFFICIENT \_ BUFFER será retornado. Essa API não pode falhar quando os parâmetros válidos são passados e um buffer grande o suficiente para manter todos os dados de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

