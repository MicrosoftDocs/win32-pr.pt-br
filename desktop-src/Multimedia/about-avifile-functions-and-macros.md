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
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="da42d-105">Sobre as funções e macros do AVIFile</span><span class="sxs-lookup"><span data-stu-id="da42d-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="da42d-106">As funções e macros do AVIFile manipulam as informações em arquivos baseados em tempo como um ou mais *fluxos de dados* em vez de blocos marcados de dados chamados partes.</span><span class="sxs-lookup"><span data-stu-id="da42d-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="da42d-107">Os fluxos de dados referem-se aos componentes de um arquivo baseado em tempo.</span><span class="sxs-lookup"><span data-stu-id="da42d-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="da42d-108">Um arquivo AVI pode conter vários tipos diferentes de dados, como uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa.</span><span class="sxs-lookup"><span data-stu-id="da42d-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="da42d-109">Usando o AVIFile, um aplicativo pode acessar cada um desses componentes separadamente.</span><span class="sxs-lookup"><span data-stu-id="da42d-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="da42d-110">Embora as funções e macros do AVIFile funcionem com qualquer arquivo RIFF, esta visão geral demonstra seu uso somente com arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="da42d-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="da42d-111">Os arquivos AVI são normalmente os arquivos baseados em tempo usados com as macros e funções do AVIFile.</span><span class="sxs-lookup"><span data-stu-id="da42d-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="da42d-112">As funções e macros AVIFile estão contidas em uma biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="da42d-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="da42d-113">Para inicializar a biblioteca, use a função [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) .</span><span class="sxs-lookup"><span data-stu-id="da42d-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="da42d-114">Depois de inicializar a biblioteca, você pode usar qualquer uma das funções ou macros AVIFile.</span><span class="sxs-lookup"><span data-stu-id="da42d-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="da42d-115">Para liberar a biblioteca, use a função [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) .</span><span class="sxs-lookup"><span data-stu-id="da42d-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="da42d-116">O AVIFile mantém uma contagem de referência dos aplicativos que estão usando a biblioteca, mas não aqueles que o lançaram.</span><span class="sxs-lookup"><span data-stu-id="da42d-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="da42d-117">Seus aplicativos devem balancear cada uso de **AVIFileInit** com uma chamada para **AVIFileExit** para liberar completamente a biblioteca depois que cada aplicativo terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="da42d-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




