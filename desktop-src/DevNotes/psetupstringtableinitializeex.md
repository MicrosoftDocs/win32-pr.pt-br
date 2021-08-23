---
description: Função pSetupStringTableInitializeEx – inicializa uma tabela de cadeia de caracteres.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Função pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 189bb94b70366ad66f0fe4dd4c4c9d5884e762cf20638f7c3ae2dc9b587f15ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538466"
---
# <a name="psetupstringtableinitializeex-function"></a>Função pSetupStringTableInitializeEx

\[Essa função não está disponível no Windows Vista ou Windows Server 2008.\]

Inicializa uma tabela de cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExtraDataSize* \[ Em\]
</dt> <dd>

Tamanho do objeto de dados extra.

</dd> <dt>

*Reservado* \[ Em\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
