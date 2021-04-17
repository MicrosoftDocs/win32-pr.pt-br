---
description: Cada evento pode ter dados específicos de eventos associados a ele.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Dados de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770420"
---
# <a name="event-data"></a>Dados de evento

Cada evento pode ter dados específicos de eventos associados a ele. O Visualizador de Eventos não interpreta esses dados; Ele exibe dados adicionais somente em um formato hexadecimal e de texto combinado. O limite máximo do tamanho de um evento no log par é de 0x3FFFF bytes. Portanto, use dados específicos de eventos com moderação, incluindo-os somente se você tiver certeza de que será útil para alguém que esteja Depurando um problema. Por exemplo, muitos eventos relacionados à rede incluem o NCB (blocos de controle de rede) como dados específicos de eventos.

Quando você usa dados específicos do evento, a última parte de sua cadeia de caracteres de descrição deve fornecer uma observação sobre as informações fornecidas como dados específicos do evento. Por exemplo, o software de rede pode fornecer uma observação como: "(o NCB são os dados de evento.)" Como uma convenção, use parênteses em relação a tais comentários, conforme indicado neste exemplo.

Você também pode usar dados específicos de eventos para armazenar informações que o aplicativo pode processar independentemente do Visualizador de Eventos. Por exemplo, você pode escrever um visualizador especificamente para seus eventos ou escrever um programa que examina o log e cria um relatório que inclui informações dos dados específicos do evento.

 

 



