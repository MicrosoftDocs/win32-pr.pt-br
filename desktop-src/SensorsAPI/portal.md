---
description: API do Sensor
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API do Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a36259910fb7583c91b695f69066aa2abf9be1e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118404"
---
# <a name="sensor-api"></a>API do Sensor

## <a name="purpose"></a>Finalidade

O Windows 7 inclui suporte nativo para sensores, que são dispositivos que podem medir fenômenos físicos, como temperatura ou localização. Esta documentação descreve a API do sensor, que permite que os aplicativos obtenham e usem dados de sensores de forma padronizada.

Como seres humanos, nós confiamos em nossos sentidos para nos fornecer informações sobre o mundo em torno dos EUA. Quando criamos máquinas para executar algum de nossos trabalhos, adicionamos mecanismos de sensor para que os computadores possam responder adequadamente às condições em constante mudança.

Por exemplo, os mecanismos de automóvel normalmente usam uma variedade de sensores. Esses sensores são monitorados por um computador integrado que ajusta continuamente as configurações, como o tempo do mecanismo, para maximizar o poder e a eficiência. Uma televisão pode usar um sensor de luz ambiente para ajustar o brilho da imagem para corresponder às condições de sala em constante mudança. Até mesmo algo tão simples quanto um botão doorbell atua como um sensor rudimentar para detectar uma presença humana na porta.

Embora o doorbell puramente mecânico atenda à sua finalidade, as informações fornecidas por sensores complexos se tornam muito mais poderosas quando combinadas com o software. Os sensores modernos podem fornecer muitos dados com muita rapidez e, em uma variedade de formatos, de forma que o software fornece um mecanismo natural para fazer sentido dos dados do sensor.

Hoje, os desenvolvedores de software podem escrever programas que usam sensores, mas a falta de padronização torna a programação de sensores uma tarefa árdua. Depois que um programa baseado em sensor é concluído, geralmente é sempre dependente de um determinado tipo de hardware. Usar uma ou mais soluções verticais para habilitar a implantação de um sistema baseado em software limitou a integração de sensores com hardware de computador e, até agora, os computadores baseados em Windows não têm nenhuma exceção.

O Windows 7 inclui suporte nativo para sensores, expandido por uma nova plataforma de desenvolvimento para trabalhar com sensores, incluindo sensores de local, como dispositivos GPS. A plataforma de sensor e localização do Windows fornece uma maneira padrão para que os fabricantes de dispositivos exponham dispositivos de sensor a desenvolvedores e consumidores de software, fornecendo aos desenvolvedores uma API (interface de programação de aplicativo) padronizada para trabalhar com sensores e dados de sensor.

Sensores são dispositivos ou mecanismos que podem medir fenômenos físicos, fornecer dados descritivos ou fornecer informações sobre o estado de um objeto ou ambiente físico. Os computadores podem fazer uso de sensores internos, sensores conectados por meio de conexões com ou sem fio, ou sensores que fornecem dados por meio de uma rede ou da Internet.

A API do sensor fornece uma maneira padrão de acessar de forma programática os dados fornecidos pelos sensores. A API do sensor padroniza:

-   Categorias, tipos e propriedades do sensor.
-   Formatos de dados para tipos de sensor padrão.
-   Interfaces COM para trabalhar com sensores e coleções de sensores.
-   Mecanismos de eventos para recebimento assíncrono de dados de sensor.

A API do sensor também permite que você defina categorias, tipos, propriedades, formatos de dados e eventos de sensor personalizados.

## <a name="developer-audience"></a>Público de desenvolvedores

A API do sensor fornece sua funcionalidade por meio de um conjunto de interfaces COM. Esta documentação pressupõe que você tenha um conhecimento prático de programação usando a linguagem de programação C++, e tenha uma compreensão básica de como usar objetos e interfaces COM. Para fins de brevidade, muitos exemplos de código nesta documentação (bem como nos exemplos de código) usam objetos Active Template Library (ATL) para implementar a funcionalidade COM.

## <a name="in-this-section"></a>Nesta seção

-   [Introdução](getting-started.md)
-   [Sobre a API do sensor](about-the-sensor-api.md)
-   [Guia de programação da API do sensor](sensor-api-programming-guide.md)
-   [Referência de programação da API do sensor](sensor-api-programming-reference.md)

 

 



