---
description: Localiza a função de destino da importação especificada e substitui o ponteiro de função na caixa de importação pelo destino da implementação da função.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Função ResolveDelayLoadedAPI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571546"
---
# <a name="resolvedelayloadedapi-function"></a>Função ResolveDelayLoadedAPI

Localiza a função de destino da importação especificada e substitui o ponteiro de função na caixa de importação pelo destino da implementação da função.

## <a name="syntax"></a>Sintaxe


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ParentModuleBase* \[ Em\]
</dt> <dd>

O endereço da base do módulo importando uma função carregada com atraso.

</dd> <dt>

*DelayloadDescriptor* \[ Em\]
</dt> <dd>

O descritor para o módulo a ser carregado.

</dd> <dt>

*FailureDllHook* \[ in, opcional\]
</dt> <dd>

O endereço do gancho de falha. Consulte [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ in, opcional\]
</dt> <dd>

O endereço do gancho de falha do sistema.

</dd> <dt>

*ThunkAddress* \[ out\]
</dt> <dd>

Os dados de thunk para a função de destino. Usado para encontrar a entrada da tabela de nomes específica da função.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Reservado; deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O endereço da importação ou o stub de falha para ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte do Linker para Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




