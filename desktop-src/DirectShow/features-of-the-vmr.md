---
description: Recursos do VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Recursos do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757687"
---
# <a name="features-of-the-vmr"></a>Recursos do VMR

O processador de mixagem de vídeo 7 (VMR-7) oferece suporte aos seguintes novos recursos:

-   Mistura real de vários fluxos de vídeo, usando os recursos de mesclagem alfa de dispositivos de hardware do Direct3D.
-   A capacidade de conectar seu próprio componente de composição para implementar efeitos e transições entre vários fluxos de vídeo entrando no VMR.
-   Renderização true sem janela. Não é mais necessário tornar a janela de reprodução de vídeo um filho da janela do aplicativo para conter reprodução de vídeo. O novo modo de renderização sem janela do VMR permite que os aplicativos hospedem facilmente a reprodução de vídeo em qualquer janela sem a necessidade de encaminhar mensagens de janela para o renderizador para processamento específico do processador.
-   Um novo modo de reprodução de renderização em que os aplicativos podem fornecer seu próprio componente de alocador para obter acesso à imagem de vídeo decodificada antes de ser exibido na tela.
-   Suporte aprimorado para PCs equipados com vários monitores.
-   Suporte para a nova arquitetura de aceleração de vídeo DirectX da Microsoft.
-   Suporte para reprodução de vídeo de alta qualidade simultaneamente em várias janelas.
-   Suporte para o modo exclusivo do DirectDraw
-   100% de compatibilidade com versões anteriores com aplicativos existentes.
-   Suporte para revisão de quadros e uma maneira confiável de capturar a imagem atual que está sendo exibida.
-   A capacidade dos aplicativos de misturar facilmente seus próprios dados estáticos de imagem (como logotipos de canal ou componentes de interface do usuário) com o vídeo de uma maneira sem cintilação suave.

O VMR-9 dá suporte a todos os recursos listados acima, além de:

-   A capacidade de processar dados de vídeo diretamente com APIs do Direct3D, como sombreadores de pixel.
-   Suporte aprimorado para conteúdo de vídeo entrelaçado.
-   Suporte em qualquer plataforma compatível com o DirectX.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o processamento de mixagem de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



