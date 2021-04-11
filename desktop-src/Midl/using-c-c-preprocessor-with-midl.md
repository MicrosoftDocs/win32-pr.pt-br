---
title: Usando C/C++-pré-processador com MIDL
description: O compilador MIDL não processa arquivos de origem.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL do compilador MIDL, pré-processador C
- MIDL de pré-processador C-pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292080"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="2fb68-105">Usando C/C++-pré-processador com MIDL</span><span class="sxs-lookup"><span data-stu-id="2fb68-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="2fb68-106">O compilador MIDL não processa arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="2fb68-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="2fb68-107">Em vez disso, o compilador MIDL usa um pré-processador disponível para preparar o fluxo de entrada para análise.</span><span class="sxs-lookup"><span data-stu-id="2fb68-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="2fb68-108">Por padrão, o MIDL usa o pré-processador para o compilador C/C++ da Microsoft a partir do mesmo ambiente de compilação que MIDL.</span><span class="sxs-lookup"><span data-stu-id="2fb68-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="2fb68-109">O usuário pode indicar um pré-processador diferente a ser usado pelo MIDL, se necessário.</span><span class="sxs-lookup"><span data-stu-id="2fb68-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="2fb68-110">O MIDL gera execuções de pré-processador separadas para arquivos IDL e ACF de nível superior e para cada arquivo importado com a diretiva de importação MIDL.</span><span class="sxs-lookup"><span data-stu-id="2fb68-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="2fb68-111">Os arquivos incluídos na diretiva **\# include** são tratados diretamente pelo pré-processador.</span><span class="sxs-lookup"><span data-stu-id="2fb68-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="2fb68-112">Os tópicos a seguir descrevem vários aspectos das interações de pré-processamento de MIDL:</span><span class="sxs-lookup"><span data-stu-id="2fb68-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="2fb68-113">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="2fb68-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="2fb68-114">Verificando opções de pré-processador</span><span class="sxs-lookup"><span data-stu-id="2fb68-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="2fb68-115">Salvando a saída do pré-processador</span><span class="sxs-lookup"><span data-stu-id="2fb68-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="2fb68-116">Lidando com as \# definições em arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="2fb68-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




