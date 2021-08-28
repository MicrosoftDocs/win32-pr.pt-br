---
description: Cada evento pode ter dados específicos do evento associados a ele.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Dados de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf6809b837d36f4cf2ddc0d74b90fe3a925f5eae7efc96973a9bf845c610bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901476"
---
# <a name="event-data"></a>Dados de evento

Cada evento pode ter dados específicos do evento associados a ele. O Visualizador de Eventos não interpreta esses dados; ele exibe dados extras somente em um formato hexadecimal e de texto combinado. O limite máximo no tamanho de um evento no log de mesmo é 0x3FFFF bytes. Portanto, use dados específicos de evento com moderação, incluindo-os somente se você tiver certeza de que eles serão úteis para alguém depurar um problema. Por exemplo, muitos eventos relacionados à rede incluem NCB (blocos de controle de rede) como dados específicos do evento.

Quando você usa dados específicos do evento, a última parte de sua cadeia de caracteres de descrição deve fornecer uma observação sobre as informações fornecidas como dados específicos do evento. Por exemplo, o software de rede pode fornecer uma observação como: "(O NCB são os dados do evento.)" Como uma convenção, use parênteses em torno desses comentários, conforme indicado neste exemplo.

Você também pode usar dados específicos do evento para armazenar informações que o aplicativo pode processar independentemente do Visualizador de Eventos. Por exemplo, você pode escrever um visualizador especificamente para seus eventos ou escrever um programa que examina o log e cria um relatório que inclui informações dos dados específicos do evento.

 

 



