---
title: Preparar seu ambiente de desenvolvimento
description: Preparar seu ambiente de desenvolvimento
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896966"
---
# <a name="prepare-your-development-environment"></a>Preparar seu ambiente de desenvolvimento

Para escrever um Windows em C ou C++, você deve instalar o SDK (Software Development Kit) do Microsoft Windows ou Microsoft Visual Studio. O Windows SDK contém os títulos e bibliotecas necessários para compilar e vincular seu aplicativo. O Windows SDK também contém ferramentas de linha de comando para criar Windows aplicativos, incluindo o compilador Visual C++ e o vinculador. Embora você possa compilar e criar Windows programas com as ferramentas de linha de comando, é recomendável usar Microsoft Visual Studio. Você pode baixar um download gratuito de Visual Studio Community ou avaliação gratuita de outras versões do Visual Studio [aqui](https://visualstudio.microsoft.com/downloads/).

Cada versão do Windows SDK tem como destino a versão mais recente do Windows, bem como várias versões anteriores. As notas sobre a versão listam as plataformas específicas com suporte, mas a menos que você esteja mantendo um aplicativo para uma versão muito antiga do Windows, instale a versão mais recente do SDK do Windows. Você pode baixar o SDK Windows mais [recente aqui.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

O Windows SDK dá suporte ao desenvolvimento de aplicativos de 32 e 64 bits. As APIs Windows são projetadas para que o mesmo código possa ser compilado para 32 bits ou 64 bits sem alterações.

> [!Note]  
> O Windows SDK não dá suporte ao desenvolvimento de driver de hardware e esta série não discutirá o desenvolvimento de driver. Para obter informações sobre como escrever um driver de hardware, [consulte Ponto de Partida com drivers Windows .](/windows-hardware/drivers/gettingstarted/)

## <a name="next"></a>Avançar

[Windows Convenções de codificação](windows-coding-conventions.md)

## <a name="related-topics"></a>Tópicos relacionados

* [Baixar o Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Baixar Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)