---
title: CSCHOBJ. CPP
description: No exemplo de componente do provedor, um exemplo de código, que gerencia o tempo de vida dos objetos de esquema, está em cschobj. cpp. Os métodos com suporte são listados na tabela a seguir.
ms.assetid: ed8cc113-2ada-4522-87b9-32c922e89819
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0159d2101a3d7728c090aa8e7d110df792c04331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634884"
---
# <a name="cschobjcpp"></a><span data-ttu-id="adfa4-104">CSCHOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="adfa4-104">CSCHOBJ.CPP</span></span>

<span data-ttu-id="adfa4-105">No exemplo de componente do provedor, um exemplo de código, que gerencia o tempo de vida dos objetos de esquema, está em cschobj. cpp.</span><span class="sxs-lookup"><span data-stu-id="adfa4-105">In the example provider component, a code example, that manages the lifetime of the schema objects, is in cschobj.cpp.</span></span> <span data-ttu-id="adfa4-106">Os métodos com suporte são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="adfa4-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="adfa4-107">Método</span><span class="sxs-lookup"><span data-stu-id="adfa4-107">Method</span></span>                                                   | <span data-ttu-id="adfa4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="adfa4-108">Description</span></span>                                    |
|----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="adfa4-109">**CSampleDSSchema:: CreateSchema**</span><span class="sxs-lookup"><span data-stu-id="adfa4-109">**CSampleDSSchema::CreateSchema**</span></span>                        | <span data-ttu-id="adfa4-110">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="adfa4-110">Standard constructor.</span></span>                          |
| <span data-ttu-id="adfa4-111">**CSampleDSSchema:: ~ CSampleDSSchema**</span><span class="sxs-lookup"><span data-stu-id="adfa4-111">**CSampleDSSchema::~CSampleDSSchema**</span></span>                    | <span data-ttu-id="adfa4-112">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="adfa4-112">Standard destructor.</span></span>                           |
| <span data-ttu-id="adfa4-113">Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) padrão.</span><span class="sxs-lookup"><span data-stu-id="adfa4-113">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                   |                                                |
| <span data-ttu-id="adfa4-114">Métodos do [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) padrão.</span><span class="sxs-lookup"><span data-stu-id="adfa4-114">Standard [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) methods.</span></span> |                                                |
| <span data-ttu-id="adfa4-115">**CSampleDSSchema:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="adfa4-115">**CSampleDSSchema::QueryInterface**</span></span>                      | <span data-ttu-id="adfa4-116">Verifique a ID de interface fornecida neste objeto.</span><span class="sxs-lookup"><span data-stu-id="adfa4-116">Verify the given interface ID on this object.</span></span>  |
| <span data-ttu-id="adfa4-117">**CSampleDSSchema::AllocateSchema**</span><span class="sxs-lookup"><span data-stu-id="adfa4-117">**CSampleDSSchema::AllocateSchema**</span></span>                      | <span data-ttu-id="adfa4-118">Crie um objeto de esquema e carregue seus dados de tipo.</span><span class="sxs-lookup"><span data-stu-id="adfa4-118">Create a schema object and load its type data.</span></span> |



 

 

 




