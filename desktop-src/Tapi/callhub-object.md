---
description: O objeto CallHub representa uma exibição de terceiros de uma chamada de várias partes.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objeto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac2f1df01479eff7688271078d2a3def2b9a35563ca9c2a4fe6533c900cda30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869980"
---
# <a name="callhub-object"></a>Objeto CallHub

O objeto CallHub representa uma exibição de terceiros de uma chamada de várias partes. As interfaces e métodos associados obterão e definirão informações sobre o hub, como se ele está ativo. Usando o objeto CallHub, um usuário com a segurança necessária pode descobrir e, potencialmente, controlar outros participantes em uma chamada.

Um objeto CallHub não pode ser criado diretamente por um aplicativo. Um objeto CallHub é criado indiretamente quando uma chamada de entrada é recebida por meio da TAPI 3.

A TAPI 3 conta com provedores de serviços TAPI para fornecer as informações necessárias sobre chamadas a implementar usando o objeto CallHub. Como nem todos os provedores de serviços fornecem essas informações e nem todos os hardwares dão suporte ao acompanhamento de hub de chamada, as informações disponíveis sobre os outros usuários na conexão podem ser limitadas ou inexistentes.

O [exemplo de código Criar uma Conferência](create-a-simple-conference.md) Simples ilustra o uso de um objeto CallHub.

Consulte [Interfaces de Objeto do CallHub](callhub-object-interfaces.md) para ver uma lista de todas as interfaces associadas ao objeto CallHub.

 

 



