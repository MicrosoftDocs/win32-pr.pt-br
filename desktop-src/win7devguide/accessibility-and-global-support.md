---
title: Acessibilidade e suporte global
description: A plataforma Windows 7 facilita a criação de soluções acessíveis a mais usuários e que atendem ou excedem os padrões de conformidade de acessibilidade.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea7f710850f419493c5a8435626d163361c8a03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084760"
---
# <a name="accessibility-and-global-support"></a>Acessibilidade e suporte global

A plataforma Windows 7 facilita a criação de soluções acessíveis a mais usuários e que atendem ou excedem os padrões de conformidade de acessibilidade. A Comunidade do ATV (fornecedor de tecnologia assistencial) agora pode criar soluções para uma variedade mais ampla de aplicativos cliente, e os desenvolvedores de aplicativos acharão mais fácil criar e validar interfaces de usuário acessíveis.

O Windows 7 também oferece suporte a várias linguagens globais mais fáceis do que nas versões anteriores do Windows. Desde o momento em que um usuário seleciona um idioma e um local, o Windows 7 apresenta datas, números, calendários, agrupamentos e outras informações usando as convenções culturais que os clientes esperam.

## <a name="windows-automation"></a>Automação do Windows

O Windows 7 oferece uma camada de automação avançada baseada em padrões que é estendida para aplicativos nativos. Ele se baseia no Microsoft Acessibilidade Ativa e na automação da interface do usuário da Microsoft. Ele também foi projetado para trabalhar com padrões do setor, como o ARIA Web do W3C (aplicativo de Internet avançado acessível) e *especificações da seção 508*.

A automação da interface do usuário oferece um desempenho aprimorado introduzindo proxies de automação não gerenciados mais rápidos para controles Microsoft Win32 e aplicativos de Microsoft Acessibilidade Ativa (*MSAA*) herdados, além de registros de proxy e eventos de automação de interface do usuário melhores e mais rápidos. Novos recursos de extensibilidade estendem padrões de controle, propriedades e eventos personalizados. (Consulte [API de automação do Windows: visão geral](../winauto/windows-automation-api-overview.md).)

## <a name="accessibility-support-tools"></a>Ferramentas de suporte de acessibilidade

O verificador de acessibilidade da interface do usuário é uma ferramenta gráfica conveniente que permite que os desenvolvedores e testadores verifiquem rapidamente se a interface de usuário está em conformidade com os principais requisitos de acessibilidade, como o *MSAA* (que verifica relações filho-pai ou retângulos delimitadores) e acesso programático à automação da interface do usuário, geração de eventos, layout e navegação de teclado. (Consulte o [Verificador de acessibilidade da interface do usuário](https://www.codeplex.com/AccCheck).)

UIA Verify é uma estrutura de automação de teste que facilita o teste manual e automatizado da implementação do provedor de automação de interface do usuário de um controle ou aplicativo. Essas duas novas ferramentas permitem que os desenvolvedores testem as implementações e funcionalidades de acessibilidade em aplicativos que usam a automação de *MSAA* ou de interface do usuário. Ambas as ferramentas estão disponíveis por meio do [codeplex](https://www.codeplex.com/), um site que a Microsoft criou para hospedar projetos de código-fonte aberto e para atender melhor à comunidade de desenvolvedores. (Consulte [verificação de automação da interface do usuário (UIA Verify) estrutura de automação de teste](https://uiautomationverify.codeplex.com/).)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Suporte aprimorado a interface do usuário em vários idiomas e serviços lingüísticos

O Windows 7 fornece aos desenvolvedores um método padrão para preparar seus aplicativos para o mercado internacional, fornecendo um suporte aprimorado à interface do usuário em vários idiomas e serviços lingüísticos que eles podem usar em seus aplicativos.

Os serviços lingüísticos estendidos são um novo recurso do Windows 7 que permite aos desenvolvedores usar o mesmo pequeno conjunto de APIs para aproveitar uma variedade de funcionalidades linguísticas avançadas. Usando os persapis linguísticas estendidos no Windows 7, os desenvolvedores podem detectar automaticamente o idioma de qualquer parte do texto Unicode e usar essas informações para ajudar a tornar as opções de experiência do usuário mais inteligentes para os clientes em todo o mundo. Os serviços lingüísticos estendidos também oferecem suporte a transliteração interna que converte o texto de um sistema de gravação em outro. Por exemplo, os desenvolvedores agora podem converter automaticamente o texto entre o chinês simplificado e o tradicional para ajudar as pessoas a se comunicarem entre os limites lingüísticos. Usando os persapis linguísticas estendidos, os desenvolvedores poderão usar os serviços lingüísticos estendidos existentes, bem como pegar novos serviços no futuro sem aprender novos códigos. (Consulte [Serviços lingüísticos estendidos](../intl/extended-linguistic-services.md).)

 

 