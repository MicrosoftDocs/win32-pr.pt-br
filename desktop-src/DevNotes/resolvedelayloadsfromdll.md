---
description: Encaminha o trabalho na resolução de importações carregadas com atraso do binário pai para um binário de destino.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Função ResolveDelayLoadsFromDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571536"
---
# <a name="resolvedelayloadsfromdll-function"></a>Função ResolveDelayLoadsFromDll

Encaminha o trabalho na resolução de importações carregadas com atraso do binário pai para um binário de destino.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ParentBase* \[ no\]
</dt> <dd>

O endereço base do módulo que atrasa a carga de outro binário.

</dd> <dt>

*TargetDllName* \[ no\]
</dt> <dd>

O nome da DLL de destino.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Reservado deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O endereço do descritor de carga de atraso, se for encontrado; caso contrário, **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte do vinculador para DLLs de Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




