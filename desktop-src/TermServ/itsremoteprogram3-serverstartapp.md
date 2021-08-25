---
title: Método ITSRemoteProgram3 ServerStartApp
description: Especifica um aplicativo para iniciar na sessão remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ServerStartApp
- Método ServerStartApp Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, método ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e162f220c59f8dfaca1d1f5666fb691ca02b8f53b5fcfe0476bf188d55b25d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072226"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>Método ITSRemoteProgram3:: ServerStartApp

Especifica um aplicativo para iniciar na sessão remota.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAppUserModelId* \[ no\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ no\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ no\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





