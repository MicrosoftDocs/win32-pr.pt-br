---
title: O ambiente
description: Os desenvolvedores que trabalham em aplicativos para o Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para o Windows de 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- Programação do ambiente de desenvolvimento de 64 bits do Windows
- Programação de ambiente de 64 bits do Windows
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, ambiente de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005187"
---
# <a name="the-environment"></a>O ambiente

Os desenvolvedores que trabalham em aplicativos para o Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para o Windows de 32 bits. As APIs existentes foram modificadas quando necessário para permitir que elas reflitam a precisão da plataforma na qual estão sendo executadas. O resultado é simplicidade e uma pequena curva de aprendizado para o desenvolvedor — escrever código para o Windows de 64 bits é como escrever código para o Windows de 32 bits.

Os arquivos de cabeçalho do Windows dão suporte a novos tipos de dados que permitem ponteiros e variáveis associadas a ponteiros para refletir a precisão da plataforma. Isso significa que os desenvolvedores podem compilar uma única base de origem para execução nativa em um Windows de 32 bits ou Windows de 64 bits. Essa estratégia reduz o custo de desenvolvimento de aplicativos que aproveitam o hardware de 64 bits, como processadores AMD Opteron ou Athlon64 ou processadores Intel Itanium.

Você terá mais tempo para tornar seus aplicativos 64-bit prontos se adotar as novas convenções de tipo de dados assim que possível. Se você estiver alterando seu código, deverá alterar as definições de dados ao mesmo tempo. Teste o aplicativo em um Windows de 32 bits, execute-o por meio do compilador de 64 bits (descrito nas [ferramentas](the-tools.md)) e o aplicativo estará pronto para teste quando você tiver o hardware de bits de 64 apropriado.

 

 




