---
description: A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitetura de DLL do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461343"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="03f40-103">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="03f40-103">Parser DLL Architecture</span></span>

<span data-ttu-id="03f40-104">A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="03f40-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="03f40-105">Lembre-se de que alguns recursos exigem a implementação de apenas um ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="03f40-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="03f40-106">No entanto, se a DLL do analisador der suporte a vários protocolos, o recurso exigirá a implementação de vários pontos de entrada.</span><span class="sxs-lookup"><span data-stu-id="03f40-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![recursos de DLL do analisador](images/parserarchitecture1.png)



| <span data-ttu-id="03f40-108">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="03f40-108">For information about</span></span>                                                  | <span data-ttu-id="03f40-109">Consulte</span><span class="sxs-lookup"><span data-stu-id="03f40-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="03f40-110">Como implementar funções de exportação de DLL do parser.</span><span class="sxs-lookup"><span data-stu-id="03f40-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="03f40-111">Gravando um analisador de protocolo</span><span class="sxs-lookup"><span data-stu-id="03f40-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="03f40-112">Funções específicas e estruturas que os analisadores usam — tópicos de referência.</span><span class="sxs-lookup"><span data-stu-id="03f40-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="03f40-113">Funções e estruturas do analisador</span><span class="sxs-lookup"><span data-stu-id="03f40-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



