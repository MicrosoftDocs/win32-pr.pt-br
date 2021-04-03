---
title: Sobre as funções e macros do AVIFile
description: Sobre as funções e macros do AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- Função AVIFileInit
- Função AVIFileExit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006130"
---
# <a name="about-avifile-functions-and-macros"></a>Sobre as funções e macros do AVIFile

As funções e macros do AVIFile manipulam as informações em arquivos baseados em tempo como um ou mais *fluxos de dados* em vez de blocos marcados de dados chamados partes. Os fluxos de dados referem-se aos componentes de um arquivo baseado em tempo. Um arquivo AVI pode conter vários tipos diferentes de dados, como uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa. Usando o AVIFile, um aplicativo pode acessar cada um desses componentes separadamente.

> [!Note]  
> Embora as funções e macros do AVIFile funcionem com qualquer arquivo RIFF, esta visão geral demonstra seu uso somente com arquivos AVI. Os arquivos AVI são normalmente os arquivos baseados em tempo usados com as macros e funções do AVIFile.

 

As funções e macros AVIFile estão contidas em uma biblioteca de vínculo dinâmico. Para inicializar a biblioteca, use a função [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) . Depois de inicializar a biblioteca, você pode usar qualquer uma das funções ou macros AVIFile. Para liberar a biblioteca, use a função [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) . O AVIFile mantém uma contagem de referência dos aplicativos que estão usando a biblioteca, mas não aqueles que o lançaram. Seus aplicativos devem balancear cada uso de **AVIFileInit** com uma chamada para **AVIFileExit** para liberar completamente a biblioteca depois que cada aplicativo terminar de usá-la.

 

 




