---
title: Desenvolver aplicativos UWP (Plataforma de Windows Universal)
description: Desenvolver aplicativos UWP (Plataforma de Windows Universal)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 332864b00614ceb494b2832c0b565a5a10819d631ecb6c4098284a94ad2c038e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935436"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Desenvolver aplicativos UWP (Plataforma de Windows Universal)

Incentivamos todos os ISVs de aplicativos da área de trabalho (Win32) a trazer seus aplicativos da área de trabalho para [a UWP (Plataforma Universal Windows)](https://developer.microsoft.com/windows/bridges/desktop/) por meio do Ponte de Desktop. Os aplicativos UWP também têm suporte na [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), portanto, é mais fácil para você atualizar os usuários para uma versão consistente automaticamente, reduzindo os custos de suporte.

Se os aplicativos da área de trabalho não puderem ser convertidos usando o Ponte de Desktop, é altamente recomendável usar um instalador que siga as práticas recomendadas e garantir que isso seja totalmente testado. Um instalador é a primeira experiência do usuário ou do cliente com seu aplicativo. Geralmente, isso não funciona bem ou não foi totalmente testado para todos os cenários. O [Kit de](https://dev.windows.com/develop/app-certification-kit) Certificação de Aplicativos do Windows pode ajudá-lo a testar a instalação e a desinstalação do aplicativo Win32 e ajudá-lo a identificar o uso de APIs não documentadas, bem como outros problemas básicos de melhores práticas relacionadas ao desempenho antes dos usuários.

## <a name="best-practices"></a>Melhores práticas:

-   Use instaladores que funcionam para versões de 32 bits e 64 bits do Windows.
-   Projete seus instaladores para execução em vários cenários (nível de usuário ou máquina).
-   Mantenha todos os recursos redistribuíveis do Windows no pacote original – se forem remontados, é possível que isso cause a perda do instalador.
-   Agende o tempo de desenvolvimento para seus instaladores. Eles geralmente são ignorados como um produto durante o ciclo de vida de desenvolvimento de software.

 

 




