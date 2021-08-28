---
description: API de localização
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19850dc1f85b227f2a5c9e03d9e0130b70c42d38e7ca0bee6308f9963042c613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693106"
---
# <a name="location-api"></a>API de localização

\[A API de Localização do Win32 e está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API. Para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Finalidade

Os computadores de hoje estão mais móveis do que nunca. De laptops pequenos a computadores Tablet, muitos computadores podem ir para onde o usuário deseja ir. Programas que aproveitam a mobilidade do computador podem agregar valor significativo às vidas das pessoas. Por exemplo, um programa que pode encontrar restaurantes próximos e fornecer instruções de condução pareceria ser um ajuste natural para um computador portátil. Mas embora a tecnologia para determinar o local atual do usuário seja comum e acessível, a criação de soluções nessa tecnologia pode ser uma tarefa difícil.

Para criar um programa com conhecimento de localização, talvez seja necessário superar uma variedade de problemas, incluindo:

-   Dispositivos GPS (sistema de posicionamento global) que usam portas COM virtuais, que fornecem acesso a apenas um programa por vez.
-   Noções básicas e de programação para protocolos, como a especificação da NMEA (National Electronics Association), bem como extensões proprietárias do fornecedor.
-   Limitando-se à programação para soluções de hardware verticais conhecidas.
-   Implementando lógica para lidar com transições entre vários provedores de localização, como receptores de GPS, redes conectadas, redes de telefone celular, Internet e configurações de usuário.

Esta documentação descreve a API (interface Windows de programação de aplicativos) local do Windows. A API de Localização ajuda a simplificar a programação com conhecimento de localização, fornecendo uma maneira padrão de recuperar dados sobre a localização do usuário e padronizar formatos para relatórios de dados de localização. A API de Localização lida automaticamente com transições entre provedores de dados de localização e sempre escolhe o provedor mais preciso para a situação atual.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de Localização fornece sua funcionalidade por meio de um conjunto de interfaces COM. A funcionalidade da API de Localização pode ser usada por programadores que estão familiarizados com o uso do COM por meio da linguagem de programação C++ ou com o uso de objetos COM em linguagens de script, como o Microsoft JScript.

## <a name="in-this-section"></a>Nesta seção

-   [Referência de programação C++ da API de Localização](windows-location-programming-reference.md)
-   [Referência do modelo de objeto da API de localização](windows-location-script-programming-reference.md)

 

 
