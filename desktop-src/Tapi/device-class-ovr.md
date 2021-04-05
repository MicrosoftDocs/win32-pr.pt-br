---
description: As classes de dispositivo simplificam o desenvolvimento, permitindo que os programadores tratem os dispositivos que têm propriedades semelhantes de maneira semelhante.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe de dispositivo (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921700"
---
# <a name="device-class"></a>Classe de dispositivo

As classes de dispositivo simplificam o desenvolvimento, permitindo que os programadores tratem os dispositivos que têm propriedades semelhantes de maneira semelhante. Por exemplo, um telefone digital em um escritório normalmente tem mais recursos do que um monofone padrão em casa, mas ambos respondem praticamente da mesma forma a um conjunto básico de funções e ambos pertencem a uma classe de dispositivo de telefone. As classes de dispositivo ajudam a tornar a TAPI extensível fornecendo uma estrutura da qual classificar e dar suporte a novos equipamentos.

Consulte [classes de dispositivo TAPI](./tapi-device-classes.md) para classes que a TAPI predefiniu. Um provedor de serviços pode implementar e definir classes de dispositivo adicionais para o equipamento que ele suporta. Um aplicativo nunca precisa saber qual provedor de serviços controla qual dispositivo, mas pode exigir informações sobre o controle de novas classes de dispositivo.

Um provedor de serviços implementa uma classe de dispositivo mapeando solicitações em comandos de dispositivo reais. Por exemplo, quando o provedor de serviços para um modem compatível com Hayes recebe um comando passado pelo TAPISVR para fazer uma chamada, ele envia comandos clássicos AT para o modem.

A interface do provedor de serviços pode ser mapeada para uma ampla variedade de ambientes, incluindo aqueles que não são tradicionalmente considerados como pertencentes a telefonia. Um exemplo é a conferência de multimídia em uma rede baseada em IP, como a Internet.

Os desenvolvedores de aplicativos devem ter em mente a existência de outros aplicativos que podem compartilhar serviços de telefonia.

 

 
