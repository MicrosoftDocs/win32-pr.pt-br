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
ms.openlocfilehash: 0ccfcb1a59f0db6d29881d139d16bd08308a40df2c1233beab66b0b4814caa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129263"
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

## <a name="return-value"></a>Valor retornado

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

 

 





