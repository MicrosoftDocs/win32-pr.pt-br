---
description: Define a atribuição de conjuntos de CPU selecionados para o thread especificado. Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Função SetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d627c3ae0499cf19ba533c30d1a3fabb05c2dbf5782d99b2f716579f50125b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031726"
---
# <a name="setthreadselectedcpusets-function"></a>Função SetThreadSelectedCpuSets

Define a atribuição de conjuntos de CPU selecionados para o thread especificado. Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Thread* \[ do no\]
</dt> <dd>

Especifica o thread no qual definir a atribuição de conjunto de CPU. Esse identificador deve ter o \_ direito de \_ acesso de informações limitadas ao conjunto de threads \_ . O valor retornado por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) também pode ser usado.

</dd> <dt>

*CpuSetIds* \[ no\]
</dt> <dd>

Especifica a lista de IDs de conjunto de CPU a ser definida como o conjunto de CPU selecionado pelo thread. Se isso for nulo, a API desmarcará qualquer atribuição, revertendo para processar a atribuição padrão se uma estiver definida.

</dd> <dt>

*CpuSetIdCount* \[ no\]
</dt> <dd>

Especifica o número de IDs na lista passada no argumento **CpuSetIds** . Se esse valor for nulo, ele deverá ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função não pode falhar quando passaram parâmetros válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
