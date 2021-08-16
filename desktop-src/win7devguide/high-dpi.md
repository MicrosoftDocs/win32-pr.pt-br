---
title: DPI alto
description: DPI alto
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5006d5bdf1c9e90745ef8e3571e64e729dbf5dff54338280789f39c6d0027e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203957"
---
# <a name="high-dpi"></a>DPI alto

À medida que as tecnologias de exibição avançam, os fabricantes aumentaram o número de pixels com suporte em suas exibições. Embora os elementos de texto, imagens e interface do usuário pareçam muito mais precisos e mais acessíveis em exibições de alta resolução, o sistema operacional deve ser escalado para dar suporte à experiência visual; caso contrário, tudo parece menor.

Windows 7 dá suporte a *exibições de DPI* alta. Os dados de mercado sugerem que as implantações de telas de *alto DPI* (120 a 144 pontos por polegada (dpi)) aumentarão no período Windows 7. Ao executar resoluções nativas nessas telas, muitos aplicativos parecem muito pequenos, a menos que usem *Alto DPI.* Alguns aplicativos (como Windows Internet Explorer) têm recursos de dimensionamento de fontes que permitem aos usuários ampliar e reduzir, mas muitos aplicativos não têm. O *recurso DPI* alto no Windows 7:

-   Garante que as Windows e as experiências do aplicativo sejam ideais no hardware padrão ( as configurações *de DPI* são otimizadas para corresponder aos recursos do hardware).
-   Permite que o Windows Shell e outros Windows aplicativos baseados em Windows pareçam bons com diferentes *configurações de DPI.*
-   Respeita as configurações *de DPI* padrão com base em especificações e funcionalidades de hardware.
-   Permite que os usuários personalizem *as configurações de DPI* sem reinicializar.
-   Garante que a tela sempre seja definida como resolução nativa.

O recurso Windows dimensionamento de *DPI* dimensiona fontes e elementos de interface do usuário (como botões, ícones e campos de entrada) por um percentual calculado, conforme especificado pela configuração *de DPI.* Isso é diferente do dimensionamento que ocorre quando a resolução de exibição é baixada. No caso do dimensionamento *de DPI,* o Windows fornece fontes e elementos de interface do usuário que são desenhados com mais pixels, resultando em uma maior, maior fidelidade e mais Windows experiência. Aplicativos de Windows de terceiros podem aproveitar as configurações de *Alto DPI* e ajustar a interface do usuário de acordo, declarando-se com alto *conhecimento de DPI.* Os desenvolvedores de aplicativos não devem mais assumir que 96 dpi é a resolução ideal para todos os aplicativos.

Para obter mais informações sobre *alto DPI* e sobre como escrever aplicativos com alto *conhecimento de DPI,* consulte [Alto DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 
