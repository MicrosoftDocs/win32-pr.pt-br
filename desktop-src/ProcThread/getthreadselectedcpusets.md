---
description: Retorna a atribuição explícita de Conjunto de CPU do thread especificado, se qualquer atribuição tiver sido definida usando a API SetThreadSelectedCpuSets. Se nenhuma atribuição explícita for definida, RequiredIdCount será definido como 0 e a função retornará TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Função GetThreadSelectedCpuSets (Processthreadapi.h)
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
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978776"
---
# <a name="getthreadselectedcpusets-function"></a>Função GetThreadSelectedCpuSets

Retorna a atribuição explícita de Conjunto de CPU do thread especificado, se qualquer atribuição tiver sido definida usando a API [**SetThreadSelectedCpuSets.**](setthreadselectedcpusets.md) Se nenhuma atribuição explícita for definida, **RequiredIdCount** será definido como 0 e a função retornará TRUE.

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

*Thread* \[ Em\]
</dt> <dd>

Especifica o thread para o qual consultar os Conjuntos de CPU selecionados. Esse handle deve ter o direito de \_ acesso THREAD QUERY \_ LIMITED \_ INFORMATION. O valor retornado por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) também pode ser especificado aqui.

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

Especifica a capacidade necessária do buffer para manter toda a lista de conjuntos de CPU selecionados pelo thread. No retorno bem-sucedido, isso especifica o número de IDs preenchidas no buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa API retorna TRUE em caso de êxito. Se o buffer não for grande o suficiente, o **valor GetLastError** será ERROR \_ INSUFFICIENT \_ BUFFER. Essa API não pode falhar quando os parâmetros válidos são passados e o buffer de retorno é grande o suficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

