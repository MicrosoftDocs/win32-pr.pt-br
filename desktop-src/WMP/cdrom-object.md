---
title: Objeto cdrom
description: O objeto cdrom fornece uma maneira de acessar um CD ou DVD em sua unidade.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objeto de cdrom Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104292987"
---
# <a name="cdrom-object"></a>Objeto cdrom

O objeto **cdrom** fornece uma maneira de acessar um CD ou DVD em sua unidade.

O objeto **cdrom** dá suporte às propriedades a seguir.



| Propriedade                                   | Descrição                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera a letra da unidade de CD ou DVD.                                                                                                                   |
| [playlist](cdrom-playlist.md)             | Recupera um objeto [playlist](playlist-object.md) que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD. |



 

O objeto **cdrom** dá suporte ao método a seguir.



| Método                   | Descrição                          |
|--------------------------|--------------------------------------|
| [ejeção](cdrom-eject.md) | Ejeta o CD ou DVD da unidade. |



 

O objeto **cdrom** é acessado por meio do método a seguir.



| Objeto                                        | Método                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Para fins de ilustração, Player. cdromCollection. Item (*índice*) é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




