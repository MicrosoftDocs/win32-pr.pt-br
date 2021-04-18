---
title: Desenvolver aplicativos Plataforma Universal do Windows (UWP)
description: Desenvolver aplicativos Plataforma Universal do Windows (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105788663"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Desenvolver aplicativos Plataforma Universal do Windows (UWP)

Incentivamos todos os ISVs de aplicativos de desktop (Win32) a trazer seus aplicativos de desktop para o [plataforma universal do Windows (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) por meio da ponte de desktop. Os aplicativos UWP também têm suporte na [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), portanto, é mais fácil para você atualizar os usuários para uma versão consistente automaticamente, reduzindo os custos de suporte.

Se seus aplicativos de área de trabalho não puderem ser convertidos usando a ponte de desktop, é altamente recomendável que você use um instalador que siga as práticas recomendadas e verifique se isso está totalmente testado. Um instalador é a primeira experiência do usuário ou do seu cliente com seu aplicativo. Geralmente, isso não funciona bem ou não foi totalmente testado para todos os cenários. O [Kit de certificação de aplicativos para Windows](https://dev.windows.com/develop/app-certification-kit) pode ajudá-lo a testar a instalação e a desinstalação do seu aplicativo Win32 e a identificar o uso de APIs não documentadas, bem como outros problemas básicos de práticas recomendadas relacionadas ao desempenho antes de seus usuários.

## <a name="best-practices"></a>Melhores práticas:

-   Use instaladores que funcionam para versões de 32 bits e 64 bits do Windows.
-   Projete seus instaladores para execução em vários cenários (nível de usuário ou máquina).
-   Mantenha todos os recursos redistribuíveis do Windows no pacote original – se forem remontados, é possível que isso cause a perda do instalador.
-   Agende o tempo de desenvolvimento para seus instaladores. Eles geralmente são ignorados como um produto durante o ciclo de vida de desenvolvimento de software.

 

 




