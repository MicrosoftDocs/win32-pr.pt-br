---
description: Evento que ocorre quando um novo dispositivo de hardware WIA (Aquisição de Imagem Windows Imagem) está desconectado.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento Wia.OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442152"
---
# <a name="wiaondevicedisconnected-event"></a>Evento Wia.OnDeviceDisconnected

Evento que ocorre quando um novo dispositivo de hardware WIA (Aquisição de Imagem Windows Imagem) está desconectado.

## <a name="syntax"></a>Sintaxe


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Id* 
</dt> <dd>

Uma cadeia de caracteres que contém a ID do dispositivo conectado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O WIA notifica o script ou o aplicativo sempre que um dispositivo de hardware é desconectado do computador. Implemente a sub-rotina **objWia** \_ **OnDeviceDisconnected()** para permitir que o script ou o aplicativo responda à desconexão do dispositivo.

Por exemplo, talvez você queira que um script atualize a coleção [**Dispositivos**](-wia-iwia-devices.md) quando um dispositivo for removido do computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




