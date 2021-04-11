---
title: Preparar seu ambiente de desenvolvimento
description: Preparar seu ambiente de desenvolvimento
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293992"
---
# <a name="prepare-your-development-environment"></a>Preparar seu ambiente de desenvolvimento

Para escrever um programa do Windows em C ou C++, você deve instalar o SDK (Software Development Kit) do Microsoft Windows ou o Microsoft Visual Studio. O SDK do Windows contém os cabeçalhos e as bibliotecas necessárias para compilar e vincular seu aplicativo. O SDK do Windows também contém ferramentas de linha de comando para criar aplicativos do Windows, incluindo o compilador Visual C++ e o vinculador. Embora seja possível compilar e criar programas do Windows com as ferramentas de linha de comando, é recomendável usar Microsoft Visual Studio. Você pode baixar um download gratuito da Comunidade do Visual Studio ou avaliações gratuitas de outras versões do Visual Studio [aqui](https://visualstudio.microsoft.com/downloads/).

Cada versão do SDK do Windows tem como alvo a versão mais recente do Windows, bem como várias versões anteriores. As notas de versão listam as plataformas específicas com suporte, mas, a menos que você esteja mantendo um aplicativo para uma versão muito antiga do Windows, instale a versão mais recente do SDK do Windows. Você pode baixar as SDK do Windows mais recentes [aqui](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

O SDK do Windows dá suporte ao desenvolvimento de aplicativos de 32 bits e de 64 bits. As APIs do Windows são projetadas para que o mesmo código possa Compilar para 32 bits ou 64 bits sem alterações.

> [!Note]  
> O SDK do Windows não dá suporte ao desenvolvimento de driver de hardware, e esta série não abordará o desenvolvimento de driver. Para obter informações sobre como gravar um driver de hardware, consulte [introdução com drivers do Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Avançar

[Convenções de codificação do Windows](windows-coding-conventions.md)

## <a name="related-topics"></a>Tópicos relacionados

* [Baixar o Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Baixar SDK do Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk)