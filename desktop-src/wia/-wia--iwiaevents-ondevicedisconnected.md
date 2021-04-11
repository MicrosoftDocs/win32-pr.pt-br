---
description: Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está desconectado.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
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
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169548"
---
# <a name="wiaondevicedisconnected-event"></a>Evento WIA. OnDeviceDisconnected

Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está desconectado.

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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O WIA notifica o script ou o aplicativo sempre que um dispositivo de hardware é desconectado do computador. Implemente a sub-rotina **objWia** \_ **OnDeviceDisconnected ()** para permitir que o script ou o aplicativo respondam à desconexão do dispositivo.

Por exemplo, talvez você queira que um script atualize a coleção de [**dispositivos**](-wia-iwia-devices.md) quando um dispositivo for removido do computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




