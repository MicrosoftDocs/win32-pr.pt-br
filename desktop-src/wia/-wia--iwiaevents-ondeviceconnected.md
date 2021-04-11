---
description: Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está conectado.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169549"
---
# <a name="wiaondeviceconnected-event"></a>Evento WIA. OnDeviceConnected

Evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem do Windows) está conectado.

## <a name="syntax"></a>Sintaxe


```JScript
Wia.OnDeviceConnected(
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

O WIA notifica o script ou o aplicativo sempre que um novo dispositivo de hardware estiver conectado ao computador. Implemente a sub-rotina **objWia** \_ **OnDeviceConnected ()** para permitir que o script ou o aplicativo respondam à conexão do dispositivo.

Por exemplo, talvez você queira que um script atualize a coleção de [**dispositivos**](-wia-iwia-devices.md) quando um novo dispositivo for instalado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




