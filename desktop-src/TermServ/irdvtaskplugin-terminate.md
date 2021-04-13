---
title: Método IRDVTaskPlugin Terminate
description: Chamado quando o agente de tarefa está sendo desligado.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Método Terminate Serviços de Área de Trabalho Remota
- Método Terminate Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369723"
---
# <a name="irdvtaskpluginterminate-method"></a>Método IRDVTaskPlugin:: Terminate

Chamado quando o agente de tarefa está sendo desligado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HR* \[ no\]
</dt> <dd>

Indica se o desligamento é devido a um desligamento normal ou uma falha. Se o desligamento for normal, isso conterá **S \_ OK**. Caso contrário, ele contém um código de erro **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





