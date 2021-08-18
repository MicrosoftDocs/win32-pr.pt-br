---
title: O ambiente
description: os desenvolvedores que trabalham em aplicativos para Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para Windows de 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- ambiente de desenvolvimento 64-bit Windows programação
- ambiente de 64 bits de Windows de programação
- guia de programação de Windows de 64 bits 64 – programação de Windows de bits, ambiente de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69580d6537c832abaf51b20a553c4e4e788a6013bdfc14a8002f60de9872da62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734126"
---
# <a name="the-environment"></a>O ambiente

os desenvolvedores que trabalham em aplicativos para Windows de 64 bits encontrarão o ambiente de desenvolvimento praticamente idêntico ao ambiente de desenvolvimento para Windows de 32 bits. As APIs existentes foram modificadas quando necessário para permitir que elas reflitam a precisão da plataforma na qual estão sendo executadas. o resultado é simplicidade e uma pequena curva de aprendizado para o desenvolvedor — escrever código para Windows de 64 bits é exatamente como escrever código para Windows de 32 bits.

os arquivos de cabeçalho Windows dão suporte a novos tipos de dados que permitem ponteiros e variáveis associadas a ponteiros para refletir a precisão da plataforma. isso significa que os desenvolvedores podem compilar uma única base de origem para execução nativa em Windows de 32 bits ou 64 Windows de bits. Essa estratégia reduz o custo de desenvolvimento de aplicativos que aproveitam o hardware de 64 bits, como processadores AMD Opteron ou Athlon64 ou processadores Intel Itanium.

Você terá mais tempo para tornar seus aplicativos 64-bit prontos se adotar as novas convenções de tipo de dados assim que possível. Se você estiver alterando seu código, deverá alterar as definições de dados ao mesmo tempo. teste o aplicativo em Windows de 32 bits, execute-o por meio do compilador de 64 bits (descrito nas [ferramentas](the-tools.md)) e o aplicativo estará pronto para teste quando você tiver o hardware de bits de 64 apropriado.

 

 




