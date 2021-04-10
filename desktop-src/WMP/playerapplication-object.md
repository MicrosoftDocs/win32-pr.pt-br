---
title: Objeto PlayerApplication
description: O objeto PlayerApplication fornece uma maneira de coordenar a alternância entre um controle do Windows Media Player remoto e o modo completo do Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objeto PlayerApplication Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293427"
---
# <a name="playerapplication-object"></a>Objeto PlayerApplication

O objeto **PlayerApplication** fornece uma maneira de coordenar a alternância entre um controle do Windows Media Player remoto e o modo completo do Windows Media Player. Esse objeto é usado somente com programas C++ que implementam a interface **IWMPRemoteMediaServices** e inserem o controle Player no modo remoto. Arquivos de capa usados como interfaces personalizadas para o controle remoto do Windows Media Player acessam esse objeto no código de script por meio do atributo global **playerApplication** .

O objeto **PlayerApplication** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player. |
| [playerDocked](playerapplication-playerdocked.md) | Recupera um valor que indica se o Windows Media Player está em um estado encaixado.                          |



 

O objeto **PlayerApplication** dá suporte aos métodos a seguir.



| Método                                                                       | Descrição                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Alterna um controle do Windows Media Player remoto para o estado encaixado.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Alterna um controle remoto do Windows Media Player para o modo completo do Player. |



 

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

 

 




