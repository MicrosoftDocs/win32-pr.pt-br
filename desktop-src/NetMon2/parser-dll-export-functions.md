---
description: As funções, listadas na tabela a seguir, são pontos de entrada para DLLs do analisador. As funções são os pontos de entrada para chamadas do sistema operacional e Monitor de Rede.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funções de exportação de DLL do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370594"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="a11a2-104">Funções de exportação de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="a11a2-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="a11a2-105">As funções, listadas na tabela a seguir, são pontos de entrada para DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="a11a2-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="a11a2-106">As funções são os pontos de entrada para chamadas do sistema operacional e Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="a11a2-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="a11a2-107">Função</span><span class="sxs-lookup"><span data-stu-id="a11a2-107">Function</span></span>                                           | <span data-ttu-id="a11a2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a11a2-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a11a2-109">Analisador DllMain</span><span class="sxs-lookup"><span data-stu-id="a11a2-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="a11a2-110">Indica para a DLL do analisador que está carregada ou descarregada.</span><span class="sxs-lookup"><span data-stu-id="a11a2-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="a11a2-111">O sistema operacional chama a função de **analisador DllMain** quando um processo carrega ou descarrega a dll.</span><span class="sxs-lookup"><span data-stu-id="a11a2-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="a11a2-112">Anexarproperties</span><span class="sxs-lookup"><span data-stu-id="a11a2-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="a11a2-113">Notifica o analisador para anexar qualquer propriedade existente em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a11a2-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="a11a2-114">Cancelar registro</span><span class="sxs-lookup"><span data-stu-id="a11a2-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="a11a2-115">Notifica o analisador para limpar.</span><span class="sxs-lookup"><span data-stu-id="a11a2-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="a11a2-116">Formatproperties</span><span class="sxs-lookup"><span data-stu-id="a11a2-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="a11a2-117">Notifica o analisador para pegar todas as instâncias de propriedade no e criar o membro **szPropertyText** de cada estrutura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="a11a2-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="a11a2-118">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="a11a2-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="a11a2-119">Determina se o analisador pode interpretar os dados de quadro não processados com o protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="a11a2-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="a11a2-120">Registrar analisador</span><span class="sxs-lookup"><span data-stu-id="a11a2-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="a11a2-121">Determina as informações básicas sobre o analisador dentro da DLL.</span><span class="sxs-lookup"><span data-stu-id="a11a2-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="a11a2-122">Monitor de Rede chama a função de **analisador de registro** .</span><span class="sxs-lookup"><span data-stu-id="a11a2-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="a11a2-123">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="a11a2-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="a11a2-124">Instala automaticamente um analisador.</span><span class="sxs-lookup"><span data-stu-id="a11a2-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="a11a2-125">Monitor de Rede fornece estruturas e funções auxiliares que o analisador pode chamar.</span><span class="sxs-lookup"><span data-stu-id="a11a2-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="a11a2-126">Para saber mais sobre</span><span class="sxs-lookup"><span data-stu-id="a11a2-126">For more information about</span></span>                          | <span data-ttu-id="a11a2-127">Consulte</span><span class="sxs-lookup"><span data-stu-id="a11a2-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a11a2-128">Funções auxiliares que podem ser chamadas por especialistas e analisadores.</span><span class="sxs-lookup"><span data-stu-id="a11a2-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="a11a2-129">Funções comuns de expert e parser</span><span class="sxs-lookup"><span data-stu-id="a11a2-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="a11a2-130">Funções auxiliares que somente analisadores podem chamar.</span><span class="sxs-lookup"><span data-stu-id="a11a2-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="a11a2-131">Funções do analisador</span><span class="sxs-lookup"><span data-stu-id="a11a2-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="a11a2-132">Estruturas usadas por funções de analisador.</span><span class="sxs-lookup"><span data-stu-id="a11a2-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="a11a2-133">Estruturas do analisador</span><span class="sxs-lookup"><span data-stu-id="a11a2-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



