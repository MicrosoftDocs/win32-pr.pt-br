---
title: Método OnWarning IMsTscAxEvents
description: Chamado quando o controle do cliente encontra uma condição de erro que não é fatal.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Método OnWarning Serviços de Área de Trabalho Remota
- Método OnWarning Serviços de Área de Trabalho Remota interface , IMsTscAxEvents
- Interface IMsTscAxEvents Serviços de Área de Trabalho Remota , método OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbcebe5c86bb50913ba11d4485f30757f399467aa30730f8cd27de50e360c0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657136"
---
# <a name="imstscaxeventsonwarning-method"></a>Método IMsTscAxEvents::OnWarning

Chamado quando o controle do cliente encontra uma condição de erro que não é fatal.

## <a name="syntax"></a>Sintaxe


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*warningCode* \[ Em\]
</dt> <dd>

O código de erro.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

O cache de bitmap está corrompido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





