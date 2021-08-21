---
title: Objeto PlayerApplication
description: o objeto PlayerApplication fornece uma maneira de coordenar a alternância entre um controle de Windows Media Player remoto e o modo completo de Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Windows Media Player de objeto PlayerApplication
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46ac009ead54fc4d32b1a302f9228f84484ba6911b353ebb5443653378d9ce61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571827"
---
# <a name="playerapplication-object"></a>Objeto PlayerApplication

o objeto **PlayerApplication** fornece uma maneira de coordenar a alternância entre um controle de Windows Media Player remoto e o modo completo de Windows Media Player. Esse objeto é usado somente com programas C++ que implementam a interface **IWMPRemoteMediaServices** e inserem o controle Player no modo remoto. arquivos de capa usados como interfaces personalizadas para o controle de Windows Media Player remoto acessam esse objeto no código de script por meio do atributo global **playerApplication** .

O objeto **PlayerApplication** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Windows Media Player remoto. |
| [playerDocked](playerapplication-playerdocked.md) | recupera um valor que indica se Windows Media Player está em um estado encaixado.                          |



 

O objeto **PlayerApplication** dá suporte aos métodos a seguir.



| Método                                                                       | Descrição                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | alterna um controle de Windows Media Player remoto para o estado encaixado.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | alterna um controle de Windows Media Player remoto para o modo completo do Player. |



 

O objeto **PlayerApplication** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                                          |
|-----------------------------|---------------------------------------------------|
| [Jogador](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




