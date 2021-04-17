---
description: O ELS dá suporte às funções definidas na tabela a seguir.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funções de serviços linguísticas estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747358"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="ad096-103">Funções de serviços linguísticas estendidos</span><span class="sxs-lookup"><span data-stu-id="ad096-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="ad096-104">O ELS dá suporte às funções definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad096-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="ad096-105">Função</span><span class="sxs-lookup"><span data-stu-id="ad096-105">Function</span></span>                                                 | <span data-ttu-id="ad096-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad096-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad096-107">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="ad096-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="ad096-108">Uma função de retorno de chamada definida pelo aplicativo que processa de forma assíncrona os dados produzidos pela função **MappingRecognizeText** .</span><span class="sxs-lookup"><span data-stu-id="ad096-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="ad096-109">**MappingDoAction**</span><span class="sxs-lookup"><span data-stu-id="ad096-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="ad096-110">Faz com que um serviço ELS execute uma ação após a ocorrência do reconhecimento de texto.</span><span class="sxs-lookup"><span data-stu-id="ad096-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="ad096-111">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="ad096-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="ad096-112">Libera memória e recursos alocados durante uma operação de reconhecimento de texto ELS.</span><span class="sxs-lookup"><span data-stu-id="ad096-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="ad096-113">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="ad096-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="ad096-114">Libera memória e recursos alocados para o aplicativo interagir com um ou mais serviços ELSs.</span><span class="sxs-lookup"><span data-stu-id="ad096-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="ad096-115">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="ad096-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="ad096-116">Recupera uma lista de serviços disponíveis com suporte da plataforma ELS, juntamente com informações associadas, de acordo com os critérios especificados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad096-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="ad096-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="ad096-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="ad096-118">Chamadas em um serviço ELS para reconhecer texto.</span><span class="sxs-lookup"><span data-stu-id="ad096-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



