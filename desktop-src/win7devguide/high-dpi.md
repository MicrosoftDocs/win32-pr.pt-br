---
title: DPI alto
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007952"
---
# <a name="high-dpi"></a>DPI alto

À medida que as tecnologias de exibição avançam, os fabricantes aumentaram o número de pixels com suporte em suas telas. Enquanto os elementos de texto, imagens e interface do usuário parecem muito mais nítidos e legíveis em exibições de alta resolução, o sistema operacional deve escalar verticalmente para dar suporte à experiência visual; caso contrário, tudo parece menor.

O Windows 7 oferece suporte a monitores de *dpi* alto. Os dados do mercado sugerem que as implantações de telas de alto *dpi* (120-144 pontos por polegada (DPI)) aumentarão no período de tempo do Windows 7. Ao executar resoluções nativas nessas telas, muitos aplicativos parecem muito pequenos, a menos que usem *DPI alto*. Alguns aplicativos (como o Windows Internet Explorer) têm recursos de dimensionamento de fontes que permitem aos usuários ampliar e reduzir, mas muitos aplicativos não têm. O recurso de *DPI alto* no Windows 7:

-   Garante que as experiências do Windows e do aplicativo sejam ideais no hardware padrão (as configurações de *dpi* são otimizadas para corresponder aos recursos do hardware).
-   Permite que o Shell do Windows e outros aplicativos baseados no Windows pareçam bons com configurações de *dpi* diferentes.
-   Respeita as configurações de *dpi* padrão com base em especificações e recursos de hardware.
-   Permite que os usuários personalizem as configurações de *dpi* sem reinicializar.
-   Garante que a tela seja sempre definida como resolução nativa.

O recurso de dimensionamento de *dpi* do Windows dimensiona fontes e elementos da interface do usuário (como botões, ícones e campos de entrada) por uma porcentagem calculada, conforme especificado pela configuração de *dpi* . Isso é diferente do dimensionamento que ocorre quando a resolução de vídeo é reduzida. No caso do ajuste de *dpi* , o Windows fornece fontes e elementos de interface do usuário que são desenhados com mais pixels, resultando em uma experiência maior, de maior fidelidade e mais nítida do Windows. Os aplicativos do Windows de terceiros podem aproveitar as configurações de *DPI alto* e ajustar a interface do usuário de forma adequada, declarando-se com reconhecimento de *DPI alto* . Os desenvolvedores de aplicativos não devem mais supor que 96 DPI é a resolução ideal para todos os aplicativos.

Para obter mais informações sobre *dpi alta* e sobre como escrever aplicativos com reconhecimento de *dpi alta* , consulte [DPI alto](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 