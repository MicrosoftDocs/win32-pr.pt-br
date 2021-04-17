---
description: Localiza a função de destino da importação especificada e substitui o ponteiro de função na conversão de importação pelo destino da implementação da função.
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
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749407"
---
# <a name="resolvedelayloadedapi-function"></a>Função ResolveDelayLoadedAPI

Localiza a função de destino da importação especificada e substitui o ponteiro de função na conversão de importação pelo destino da implementação da função.

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

*ParentModuleBase* \[ no\]
</dt> <dd>

O endereço da base do módulo que importa uma função carregada com atraso.

</dd> <dt>

*DelayloadDescriptor* \[ no\]
</dt> <dd>

O descritor do módulo a ser carregado.

</dd> <dt>

*FailureDllHook* \[ em, opcional\]
</dt> <dd>

O endereço do gancho de falha. Consulte [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ em, opcional\]
</dt> <dd>

O endereço do gancho de falha do sistema.

</dd> <dt>

*ThunkAddress* \[ fora\]
</dt> <dd>

Os dados de conversão para a função de destino. Usado para localizar a entrada da tabela de nome específico da função.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Reservado deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O endereço da importação ou o stub de falha para ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte do vinculador para DLLs de Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




