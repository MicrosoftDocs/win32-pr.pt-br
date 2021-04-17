---
description: Recupera o tipo de dispositivo de hardware de aquisição de imagem do Windows (WIA).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: Propriedade DeviceInfo. Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766555"
---
# <a name="deviceinfotype-property"></a>Propriedade DeviceInfo. Type

Recupera o tipo de dispositivo de hardware de aquisição de imagem do Windows (WIA). Os valores possíveis são:

-   DigitalCamera
-   Scanner
-   StreamingVideo
-   Padrão

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres que recebe o dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




