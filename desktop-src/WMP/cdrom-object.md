---
title: Objeto Cdrom
description: O objeto Cdrom fornece uma maneira de acessar um CD ou DVD em sua unidade.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Cdrom Object Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60c4e1081dec3e44107778e45fd911e0c4bb673d27b5e19874508ddbacb270ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342639"
---
# <a name="cdrom-object"></a>Objeto Cdrom

O **objeto Cdrom** fornece uma maneira de acessar um CD ou DVD em sua unidade.

O **objeto Cdrom** dá suporte às propriedades a seguir.



| Propriedade                                   | Descrição                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera a letra da unidade de CD ou DVD.                                                                                                                   |
| [Lista](cdrom-playlist.md)             | Recupera um [objeto Playlist](playlist-object.md) que representa as faixas no CD atualmente na unidade de CD ou nas entradas de título de nível raiz para DVD. |



 

O **objeto Cdrom** dá suporte ao método a seguir.



| Método                   | Descrição                          |
|--------------------------|--------------------------------------|
| [Ejetar](cdrom-eject.md) | Ejeta o CD ou DVD da unidade. |



 

O **objeto Cdrom** é acessado por meio do método a seguir.



| Objeto                                        | Método                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Para fins de ilustração, player.cdromCollection.item(*index*) é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




