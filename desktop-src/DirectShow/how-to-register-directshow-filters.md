---
description: Como registrar filtros do DirectShow
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Como registrar filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370177"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="ca2eb-103">Como registrar filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca2eb-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="ca2eb-104">Este artigo descreve como fazer o registro automático de um filtro do Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ca2eb-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="ca2eb-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="ca2eb-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="ca2eb-106">Layout das chaves do registro</span><span class="sxs-lookup"><span data-stu-id="ca2eb-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="ca2eb-107">Declarando informações de filtro</span><span class="sxs-lookup"><span data-stu-id="ca2eb-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="ca2eb-108">Declarando o modelo de fábrica</span><span class="sxs-lookup"><span data-stu-id="ca2eb-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="ca2eb-109">Implementando DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="ca2eb-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="ca2eb-110">Diretrizes para o registro de filtros</span><span class="sxs-lookup"><span data-stu-id="ca2eb-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="ca2eb-111">Cancelando o registro de um filtro</span><span class="sxs-lookup"><span data-stu-id="ca2eb-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="ca2eb-112">Este artigo não descreve como criar uma DLL para um filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ca2eb-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="ca2eb-113">Para obter informações sobre como criar DLLs, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="ca2eb-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca2eb-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca2eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca2eb-115">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="ca2eb-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



