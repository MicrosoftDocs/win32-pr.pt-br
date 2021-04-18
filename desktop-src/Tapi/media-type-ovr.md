---
description: O tipo de mídia (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa. Um determinado dispositivo pode ser capaz de manipular apenas um tipo de mídia, ou pode ser capaz de lidar com um intervalo de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759044"
---
# <a name="media-type"></a>Tipo de Mídia

O *tipo de mídia* (ou modo) de um dispositivo descreve o tipo de informações que podem ser trocadas, como voz interativa. Um determinado dispositivo pode ser capaz de manipular apenas um tipo de mídia, ou pode ser capaz de lidar com um intervalo de tipos.

Os provedores de serviço expõem o tipo de mídia ou os tipos com suporte pelos dispositivos que eles controlam. Os aplicativos consultam o tipo de mídia e, em seguida, usam essas informações para selecionar um endereço apropriado no qual iniciar uma sessão. A resposta do aplicativo para uma sessão oferecida também pode ser predicada no tipo de mídia.

Uma determinada sessão de comunicação, ou chamada, pode envolver vários tipos de mídia. Para obter mais informações, consulte tipo de mídia para uma sessão.

**TAPI 2. x:** Consulte [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), membro **DwAvailableMediaModes** da estrutura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) apontado por *lpAddressCaps*, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).

**TAPI 3. x:** Consulte [**ITTerminal:: get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).
