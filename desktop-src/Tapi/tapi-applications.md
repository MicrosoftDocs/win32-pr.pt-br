---
description: O material a seguir fornece diretrizes sobre como usar a TAPI para escrever aplicativos de usuário final ou de comunicação de servidor. Essas informações também são altamente relevantes para os programadores de provedores de serviços.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Aplicativos TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757198"
---
# <a name="tapi-applications"></a>Aplicativos TAPI

O material a seguir fornece diretrizes sobre como usar a TAPI para escrever aplicativos de usuário final ou de comunicação de servidor. Essas informações também são altamente relevantes para os programadores de provedores de serviços.

A primeira decisão que um programador precisa fazer no uso da TAPI é o nível de serviço necessário. Por exemplo, se um aplicativo exigir uma seleção de menu que possa discar um número de telefone, um aplicativo TAPI completo provavelmente não será necessário. A telefonia assistida pode habilitar essa opção de forma rápida e simples. Consulte [os níveis de serviço TAPI](tapi-levels-of-service.md) para obter mais informações sobre a distinção entre aplicativos TAPI completos e telefonia assistida.

A segunda decisão importante é se usar a TAPI 2. x, a API baseada em C ou a TAPI 3. x, que se baseia em COM. Consulte [TAPI 3. x vs. TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) para obter uma discussão sobre considerações importantes para decidir qual delas usar.

O diagrama a seguir ilustra os blocos de construção básicos de um aplicativo TAPI completo. A TAPI 2. x e a TAPI 3. x são abordadas nessas seções. Material que é altamente específico de um é abordado nas seções de visão geral para TAPI 2. x ou TAPI 3. x.

![blocos de construção de um aplicativo TAPI](images/tapior3.png)

Os links a seguir fornecem conteúdo que corresponde às figuras na imagem acima:

| Figuras | Documentação                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [Inicialização TAPI](tapi-initialization.md)                                   |
| 2      | [Controle de sessão](session-control.md)                                           |
| 3      | [Controle de dispositivo](device-control.md)                                             |
| 4      | [Controle de mídia](media-control.md)                                               |
| 5      | [Sobre controles do Call Center](about-call-center-controls.md)                     |
| 6      | [Conferência de telefonia IP de reunião](rendezvous-ip-telephony-conferencing.md) |
| 7      | [Desligamento TAPI](tapi-shutdown.md)                                               |



 

 

 



