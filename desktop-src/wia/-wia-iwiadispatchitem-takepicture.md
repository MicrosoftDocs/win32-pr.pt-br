---
description: O método TakePicture do objeto item faz com que um dispositivo de câmera digital pegue uma imagem e retorna um objeto item que representa a imagem resultante. Esse método se aplica somente a dispositivos de câmera digital.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Método item. TakePicture (Wiavideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921800"
---
# <a name="itemtakepicture-method"></a>Método item. TakePicture

O método **TakePicture** do objeto [**Item**](-wia-item.md) faz com que um dispositivo de câmera digital pegue uma imagem e retorna um objeto **Item** que representa a imagem resultante. Esse método se aplica somente a dispositivos de câmera digital.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **IWiaDispatchItem**

Um objeto [**Item**](-wia-item.md) que representa a imagem que esse método cria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wiavideo. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




