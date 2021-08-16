---
description: evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem Windows) está conectado.
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
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209543"
---
# <a name="wiaondeviceconnected-event"></a>Evento WIA. OnDeviceConnected

evento que ocorre quando um novo dispositivo de hardware WIA (aquisição de imagem Windows) está conectado.

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

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O WIA notifica o script ou o aplicativo sempre que um novo dispositivo de hardware estiver conectado ao computador. Implemente a sub-rotina **objWia** \_ **OnDeviceConnected ()** para permitir que o script ou o aplicativo respondam à conexão do dispositivo.

Por exemplo, talvez você queira que um script atualize a coleção de [**dispositivos**](-wia-iwia-devices.md) quando um novo dispositivo for instalado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




