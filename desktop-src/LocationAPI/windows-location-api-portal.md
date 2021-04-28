---
description: API de localização
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e9dccf5f88da1c608cfbc03898899f171a2627
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110884"
---
# <a name="location-api"></a>API de localização

\[A API do local do Win32 e está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) . Para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Finalidade

Atualmente, os computadores estão mais móveis do que nunca. De laptops pequenos a Tablet PCs, muitos computadores podem ir onde quer que o usuário queira ir. Os programas que tiram proveito da mobilidade do computador podem agregar valor significativo às vidas das pessoas. Por exemplo, um programa que pode encontrar restaurantes próximos e fornecer indicações pareceria ser uma opção natural para um computador portátil. Mas, embora a tecnologia para determinar o local atual do usuário seja comum e acessível, a criação de soluções nessa tecnologia pode ser uma tarefa assustadora.

Para criar um programa com reconhecimento de local, talvez seja necessário superar uma variedade de problemas, incluindo:

-   Dispositivos GPS (Global Positioning System) que usam portas COM virtuais, que fornecem acesso a apenas um programa por vez.
-   Compreensão e programação de protocolos, como a especificação NMEA (National náuticos Electronics Association), bem como extensões de fornecedores proprietários.
-   Estar confinado em programação para soluções de hardware conhecidas e verticais.
-   Implementar a lógica para lidar com transições entre vários provedores de locais, como receptores de GPS, redes conectadas, redes de telefone celular, Internet e configurações de usuário.

Esta documentação descreve a API (interface de programação de aplicativo) do local do Windows. A API de localização ajuda a simplificar a programação com reconhecimento de local, fornecendo uma maneira padrão de recuperar dados sobre o local do usuário e padronizar formatos para relatórios de dados de localização. A API de localização manipula automaticamente as transições entre os provedores de dados de localização e sempre escolhe o provedor mais preciso para a situação atual.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de localização fornece sua funcionalidade por meio de um conjunto de interfaces COM. A funcionalidade da API de localização pode ser usada por programadores que estão familiarizados com o uso de COM por meio da linguagem de programação C++ ou com objetos COM em linguagens de script, como o Microsoft JScript.

## <a name="in-this-section"></a>Nesta seção

-   [Referência de programação de C++ da API de localização](windows-location-programming-reference.md)
-   [Referência de modelo de objeto de API de localização](windows-location-script-programming-reference.md)

 

 
