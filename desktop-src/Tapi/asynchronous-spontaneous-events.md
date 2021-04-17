---
description: Há outra classe de eventos assíncronos além daquelas descritas acima.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventos ESPONTANEOS assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780127"
---
# <a name="asynchronous-spontaneous-events"></a>Eventos ESPONTANEOS assíncronos

Há outra classe de eventos assíncronos além daquelas descritas acima. Esses eventos são "ESPONTANEOS", no sentido de que não são resultados diretos de solicitações correspondentes. Esses eventos são detectados nesses casos como quando uma chamada de entrada chega ou quando uma chamada de saída passa de um "toque" para um estado de "resposta". Quando a TAPI Inicializa pela primeira vez as interações com o TSPI para um dispositivo específico, ele passa um ponteiro para um procedimento de retorno de chamada a ser chamado para relatar esses eventos ESPONTANEOS. Juntamente com este ponteiro de procedimento há um identificador de dispositivo que o provedor de serviços inclui como um dos parâmetros reais para o retorno de chamada.

 

 



