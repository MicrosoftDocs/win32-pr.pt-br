---
description: Retorna a atribuição de conjunto de CPU explícita do thread especificado, se qualquer atribuição tiver sido definida usando a API SetThreadSelectedCpuSets. Se nenhuma atribuição explícita for definida, RequiredIdCount será definido como 0 e a função retornará TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Função GetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011020"
---
# <a name="getthreadselectedcpusets-function"></a>Função GetThreadSelectedCpuSets

Retorna a atribuição de conjunto de CPU explícita do thread especificado, se qualquer atribuição tiver sido definida usando a API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) . Se nenhuma atribuição explícita for definida, **RequiredIdCount** será definido como 0 e a função retornará true.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Thread* \[ do no\]
</dt> <dd>

Especifica o thread para o qual consultar os conjuntos de CPU selecionados. Esse identificador deve ter o \_ direito de \_ acesso a informações limitadas à consulta de thread \_ . O valor retornado por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) também pode ser especificado aqui.

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

Especifica a capacidade necessária do buffer para manter a lista completa de conjuntos de CPU selecionados de thread. Após o retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa API retorna TRUE em caso de êxito. Se o buffer não for grande o suficiente, o valor **GetLastError** será um \_ buffer insuficiente de erro \_ . Esta API não pode falhar quando passou parâmetros válidos e o buffer de retorno é grande o suficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows 10 \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2016 \[ Desktop aplicativos \| UWP\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

