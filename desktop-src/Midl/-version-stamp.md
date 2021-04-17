---
title: opção/version_stamp
description: A \_ opção de carimbo/Version suprime a geração de macros que especificam o número de versão mínimo necessário do arquivo de cabeçalho RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp MIDL do comutador
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105812920"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="44d36-104">\_opção de carimbo/Version</span><span class="sxs-lookup"><span data-stu-id="44d36-104">/version\_stamp switch</span></span>

<span data-ttu-id="44d36-105">A opção de **\_ carimbo/Version** suprime a geração de macros que especificam o número de versão mínimo necessário do arquivo de cabeçalho RPC, Rpcndr. h.</span><span class="sxs-lookup"><span data-stu-id="44d36-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="44d36-106">Os novos recursos de MIDL podem exigir definições adicionais para compilar o stub corretamente, portanto, o stub tem macros que verificam a compatibilidade entre arquivos binários de MIDL e o ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="44d36-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="44d36-107">Talvez seja necessário usar essa opção se você mover MIDL para um ambiente de compilação diferente daquele em que você instalou os arquivos binários de MIDL pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="44d36-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="44d36-108">Observe que não há suporte para a combinação de ambientes de compilação.</span><span class="sxs-lookup"><span data-stu-id="44d36-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="44d36-109">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="44d36-109">Switch Options</span></span>

<span data-ttu-id="44d36-110">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44d36-110">This switch has no parameters.</span></span>

 

 




