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
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788034"
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

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





