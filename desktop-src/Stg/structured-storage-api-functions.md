---
title: Funções de API de armazenamento estruturado
description: Algumas das funções de API para o armazenamento estruturado são funções auxiliares que executam uma sequência de chamadas para outras funções de API e métodos de interface. Você pode usar essas funções auxiliares como pequenos cortes.
ms.assetid: 99ac66bc-db73-4811-9a39-fc49bb90ada8
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, funções de API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df87e8c5910c6da23ca518d05541a69e7070f8bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291879"
---
# <a name="structured-storage-api-functions"></a><span data-ttu-id="e5ad4-105">Funções de API de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="e5ad4-105">Structured Storage API Functions</span></span>

<span data-ttu-id="e5ad4-106">Algumas das funções de API para o armazenamento estruturado são funções auxiliares que executam uma sequência de chamadas para outras funções de API e métodos de interface.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-106">Some of the API functions for structured storage are helper functions that perform a sequence of calls to other API functions and interface methods.</span></span> <span data-ttu-id="e5ad4-107">Você pode usar essas funções auxiliares como pequenos cortes.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-107">You can use these helper functions as short cuts.</span></span>

<span data-ttu-id="e5ad4-108">Outras funções de API fornecem acesso à implementação do COM de armazenamento estruturado, arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-108">Other API functions provide access to COM's implementation of structured storage, Compound Files.</span></span>

<span data-ttu-id="e5ad4-109">Ainda outro conjunto de funções de API permite que você converta objetos OLE 1 em armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-109">Still another set of API functions enable you to convert OLE 1 objects to structured storage.</span></span> <span data-ttu-id="e5ad4-110">Você pode usar essas funções para determinar se uma classe de objeto é proveniente de OLE 1 e converter objetos entre os formatos de armazenamento COM OLE 1 e atual.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-110">You can use these functions to determine whether an object class is from OLE 1 and to convert objects between OLE 1 and current COM storage formats.</span></span>

<span data-ttu-id="e5ad4-111">Por fim, há funções de API para converter e emular outros objetos.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-111">Finally, there are API functions for converting and emulating other objects.</span></span> <span data-ttu-id="e5ad4-112">Essas funções fornecem serviços para um aplicativo de servidor trabalhar com dados de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-112">These functions provide services for one server application to work with data from another application.</span></span> <span data-ttu-id="e5ad4-113">Os dados podem ser convertidos para o formato nativo do aplicativo de servidor lendo os dados de seu formato original, mas gravando-os no formato nativo do aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-113">The data can be converted to the native format of the server application by reading the data from its original format but writing it in the native format of the object application.</span></span> <span data-ttu-id="e5ad4-114">Ou os dados podem permanecer em seu formato original enquanto o aplicativo de servidor lê e grava os dados em seu formato original.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-114">Or the data can remain in its original format while the server application both reads and writes the data in its original format.</span></span>

<span data-ttu-id="e5ad4-115">Para obter mais informações, consulte a seção a seguir [modos de acesso estruturado de armazenamento](structured-storage-access-modes.md).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-115">For more information, see the following section [Structured Storage Access Modes](structured-storage-access-modes.md).</span></span>

 

 




