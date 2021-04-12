---
description: A tecnologia de memória persistente (PM) fornece acesso em nível de byte para mídia não volátil e também reduz a latência de armazenamento ou recuperação de dados significativamente.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programação de memória persistente na integração do Windows-NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171599"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programação de memória persistente na integração do Windows-NVML

A tecnologia de memória persistente (PM) fornece acesso em nível de byte para mídia não volátil e também reduz a latência de armazenamento ou recuperação de dados significativamente. Ele cria uma nova camada entre a memória de um sistema e o armazenamento tradicional. Qualquer programa dependente ou dimensionado com gravações rápidas para um meio persistente pode se beneficiar do PM.

A finalidade deste artigo é descrever como a biblioteca de memória não volátil (NVML) pode ser integrada a um projeto do Visual Studio para facilitar o uso.

> [!Note]  
> A memória persistente às vezes é também chamada de SCM (memória de classe de armazenamento).

 

## <a name="pm-and-nvml"></a>PM e NVML

O primeiro suporte para memória persistente foi introduzido no Windows Server 2016 e na atualização de aniversário do Windows 10 (1607). Para obter uma visão geral rápida, confira estes dois vídeos do channel9:

-   [Usando memória não volátil (NVDIMM-N) como armazenamento em bloco no Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Usando memória não volátil (NVDIMM-N) como armazenamento Byte-Addressable no Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Para ajudar os desenvolvedores a aproveitar os benefícios das ofertas de memória persistente, a Microsoft também contribuiu com os esforços de trazer a biblioteca de memória não volátil (NVML) para o Windows. Essa biblioteca fornece várias ferramentas para tornar os aplicativos cientes da memória persistente. Por exemplo, ele contém código que permite que você crie facilmente um repositório de chave-valor com reconhecimento de PM para buscas e armazenamentos extremamente rápidos. Você pode encontrar mais informações sobre o NVML, incluindo exemplos, na [biblioteca do NVM](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integrando o NVML a um projeto do Visual Studio

1. Baixar arquivos e cabeçalhos da biblioteca NVML

-   O NVML é mantido no GitHub. Você pode compilar a origem por conta própria ou apenas baixar binários compilados diretamente aqui: [NVML versão 1,2-visualização técnica do Windows](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Coloque os arquivos de biblioteca e os cabeçalhos em um diretório de sua escolha, por exemplo: "C: \\ NVML \\ lib" e "C: \\ NVML \\ Inc", respectivamente.

3. Configure seu projeto da seguinte maneira:

-   Abra seu projeto do Visual Studio e, no "Gerenciador de Soluções", clique com o botão direito do mouse no nome do seu projeto.
-   Abra o painel de configuração do projeto na parte inferior do pop-up resultante.
-   Navegue até "Propriedades de configuração-> C/C++" e adicione a pasta na qual você armazenou o cabeçalho (C: \\ NVML \\ Inc) no campo "diretórios de inclusão adicionais".
-   Em seguida, navegue até "Propriedades de configuração – vinculador >" e adicione a pasta na qual você armazenou a biblioteca (C: \\ NVML \\ lib) no campo "diretórios de biblioteca adicionais"

4. Em seguida, certifique-se de ter como destino o projeto para a atualização de aniversário do Windows Server 2016 ou do Windows 10:

-   Navegue até "Propriedades de configuração-> geral" e defina o campo "versão da plataforma de destino" como "10.0.14393.0" e
-   Navegue até "Propriedades de configuração-> C/C++" e adicione "NTDDI \_ version = NTDDI \_ WIN10 \_ RS1;" ao campo "pré-processador".

5. Incluir os cabeçalhos em seu código e vincular às bibliotecas necessárias

-   Neste ponto, você pode simplesmente incluir os arquivos de cabeçalho que você está procurando usar em seu código como qualquer outro arquivo de cabeçalho. Por exemplo, para usar libpmem:
    -   Adicione " \# include <libpmem. h>" e
    -   Adicione "libpmem. lib" a "Propriedades de configuração-> linker-> Input-> dependências adicionais"

Neste ponto, você está pronto para chamar as funções da biblioteca diretamente no seu código e tirar proveito delas.

 

 



