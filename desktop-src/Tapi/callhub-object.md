---
description: O objeto CallHub representa uma exibição de terceiros de uma chamada de multiparte.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objeto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922087"
---
# <a name="callhub-object"></a>Objeto CallHub

O objeto CallHub representa uma exibição de terceiros de uma chamada de multiparte. As interfaces e os métodos associados obtêm e definem informações relacionadas ao Hub, como se ele está ativo. Usando o objeto CallHub, um usuário com a segurança necessária pode descobrir e potencialmente controlar outros participantes em uma chamada.

Um objeto CallHub não pode ser criado diretamente por um aplicativo. Um objeto CallHub é criado indiretamente quando uma chamada de entrada é recebida por meio da TAPI 3.

A TAPI 3 conta com provedores de serviços TAPI para fornecer as informações necessárias sobre chamadas para implementar usando o objeto CallHub. Como nem todos os provedores de serviço fornecem essas informações, e nem todo o hardware dá suporte ao acompanhamento do hub de chamadas, as informações disponíveis sobre os outros usuários na conexão podem ser limitadas ou inexistentes.

O exemplo [criar um código de conferência simples](create-a-simple-conference.md) ilustra o uso de um objeto CallHub.

Consulte [interfaces de objeto CallHub](callhub-object-interfaces.md) para obter uma lista de todas as interfaces associadas ao objeto CallHub.

 

 



