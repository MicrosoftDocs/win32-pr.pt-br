---
description: O tipo de mídia (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa. Um determinado dispositivo pode ser capaz de lidar com apenas um tipo de mídia, ou pode ser capaz de lidar com uma variedade de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf79b97adb9df491aef1ff86be62fb838246c85a45b5ce251f5c0e88df5814f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002884"
---
# <a name="media-type"></a>Tipo de Mídia

O *tipo de* mídia (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa. Um determinado dispositivo pode ser capaz de lidar com apenas um tipo de mídia, ou pode ser capaz de lidar com uma variedade de tipos.

Os provedores de serviços expõem o tipo de mídia ou os tipos com suporte pelos dispositivos que eles controlam. Os aplicativos consultam o tipo de mídia e, em seguida, usam essas informações para selecionar um endereço apropriado no qual iniciar uma sessão. A resposta do aplicativo a uma sessão oferecida também pode ser predicado no tipo de mídia.

Uma determinada sessão de comunicação, ou chamada, pode envolver vários tipos de mídia. Para obter mais informações, consulte Tipo de mídia para uma sessão.

**TAPI 2.x:** Consulte [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **membro dwAvailableMediaModes** da estrutura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) apontada por *lpAddressCaps*, [ \_ Constantes LINEMEDIAMODE](./linemediamode--constants.md).

**TAPI 3.x:** Consulte [**ItTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [ \_ Constantes TAPIMEDIATYPE](tapimediatype--constants.md).
