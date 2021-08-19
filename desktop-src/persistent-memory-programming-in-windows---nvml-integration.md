---
description: A tecnologia pm (memória persistente) fornece acesso em nível de byte a mídia não volátil, reduzindo também a latência de armazenamento ou recuperação de dados significativamente.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programação de memória persistente no Windows - Integração NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750a05f28ca4698091f79b1004bbbb00ff69752e0ff45f2153cc4f0b7fe20a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951046"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programação de memória persistente no Windows - Integração NVML

A tecnologia pm (memória persistente) fornece acesso em nível de byte a mídia não volátil, reduzindo também a latência de armazenamento ou recuperação de dados significativamente. Ele cria uma nova camada entre a memória de um sistema e o armazenamento tradicional. Qualquer programa dependente ou dimensionado com gravações rápidas em um meio persistente pode se beneficiar do PM.

A finalidade deste artigo é delinear como a NVML (biblioteca de memória não volátil) pode ser integrada a um projeto Visual Studio para facilitar o uso.

> [!Note]  
> Às vezes, a memória persistente também é chamada de memória Armazenamento classe (SCM).

 

## <a name="pm-and-nvml"></a>PM e NVML

O primeiro suporte para memória persistente foi introduzido no Windows Server 2016 e na Atualização Windows 10 Aniversário (1607). Para uma visão geral rápida, confira estes dois vídeos do Channel9:

-   [Usando memória não volátil (NVDIMM-N) como bloco Armazenamento em Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Usando memória não volátil (NVDIMM-N) como Byte-Addressable Armazenamento no Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Para ajudar os desenvolvedores a aproveitarem os benefícios das ofertas de memória persistente, a Microsoft também contribuiu para os esforços de levar a NVML (biblioteca de memória não volátil) para Windows. Essa biblioteca fornece várias ferramentas para tornar os aplicativos com memória persistente ciente. Por exemplo, ele contém um código que permite criar facilmente um armazenamento de chave-valor com conhecimento de PM para buscas e armazenamentos extremamente rápidos. Você pode encontrar mais informações sobre NVML, incluindo exemplos, em [Biblioteca NVM](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integração de NVML em um Visual Studio Project

1. Baixar os arquivos e os headers da biblioteca NVML

-   NVML é mantido em GitHub. Você pode compilar a origem por conta própria ou apenas baixar binários compilados diretamente [daqui: NVML versão 1.2 – Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Coloque os arquivos de biblioteca e os headers em um diretório de sua escolha, por exemplo: "C: \\ NVML lib" e \\ "C: \\ NVML \\ inc", respectivamente.

3. Configure seu projeto da seguinte forma:

-   Abra seu projeto do Visual Studio e, no "Gerenciador de Soluções" clique com o botão direito do mouse no nome do projeto.
-   Abra o painel de configuração do projeto na parte inferior do pop-up resultante.
-   Navegue até "Propriedades de Configuração -> C/C++" e adicione a pasta na qual você armazenou o header (C: NVML inc) ao campo "Diretórios de Inclusão \\ \\ Adicionais".
-   Em seguida, navegue até "Propriedades de configuração -> Linker" e adicione a pasta na qual você armazenou a biblioteca (C: NVML lib) ao campo "Diretórios adicionais da \\ \\ biblioteca"

4. Em seguida, certifique-se de direcionar o projeto para Windows Server 2016 ou Windows 10 De aniversário:

-   Navegue até "Propriedades de Configuração -> Geral" e de definir o campo "Versão da Plataforma de Destino" como "10.0.14393.0" e
-   Navegue até "Propriedades de configuração -> C/C++" e adicione "NTDDI \_ VERSION=NTDDI \_ WIN10 \_ RS1;" ao campo "Pré-processador".

5. Inclua os títulos em seu código e vincule às bibliotecas necessárias

-   Neste ponto, você pode simplesmente incluir os arquivos de header que você está procurando usar em seu código, como qualquer outro arquivo de header. Por exemplo, para usar libpmem:
    -   add " \# include <libpmem.h>" e
    -   adicione "libpmem.lib" a "Propriedades de configuração -> Linker -> Entrada -> Dependências Adicionais"

Neste ponto, você está pronto para chamar as funções da biblioteca diretamente em seu código e tirar proveito delas.

 

 



