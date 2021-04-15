---
title: CNAMESP. CPP
description: No componente de provedor de exemplo, o código que gerencia o tempo de vida do objeto de exemplo de namespace de componente de provedor está em cnamesp. cpp. Os métodos com suporte são listados na tabela a seguir.
ms.assetid: 2f570f87-d8c3-42b1-b8b9-758905bf4b86
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8204c953218692d91c52fb77d757b5e917264a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498604"
---
# <a name="cnamespcpp"></a><span data-ttu-id="99869-104">CNAMESP. CPP</span><span class="sxs-lookup"><span data-stu-id="99869-104">CNAMESP.CPP</span></span>

<span data-ttu-id="99869-105">No componente de provedor de exemplo, o código que gerencia o tempo de vida do objeto de exemplo de namespace de componente de provedor está em cnamesp. cpp.</span><span class="sxs-lookup"><span data-stu-id="99869-105">In the example provider component, code that manages the lifetime of the example provider component namespace object is in cnamesp.cpp.</span></span> <span data-ttu-id="99869-106">Os métodos com suporte são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="99869-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="99869-107">Método</span><span class="sxs-lookup"><span data-stu-id="99869-107">Method</span></span>                                                   | <span data-ttu-id="99869-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="99869-108">Description</span></span>                                            |
|----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="99869-109">**CSampleDSNamespace::CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="99869-109">**CSampleDSNamespace::CSampleDSNamespace**</span></span>               | <span data-ttu-id="99869-110">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="99869-110">Standard constructor.</span></span>                                  |
| <span data-ttu-id="99869-111">**CSampleDSNamespace:: ~ CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="99869-111">**CSampleDSNamespace::~CSampleDSNamespace**</span></span>              | <span data-ttu-id="99869-112">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="99869-112">Standard destructor.</span></span>                                   |
| <span data-ttu-id="99869-113">Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) padrão.</span><span class="sxs-lookup"><span data-stu-id="99869-113">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                   |                                                        |
| <span data-ttu-id="99869-114">Métodos do [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) padrão.</span><span class="sxs-lookup"><span data-stu-id="99869-114">Standard [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) methods.</span></span> |                                                        |
| <span data-ttu-id="99869-115">**CSampleDSNamespace::AllocateNamespaceObject**</span><span class="sxs-lookup"><span data-stu-id="99869-115">**CSampleDSNamespace::AllocateNamespaceObject**</span></span>          | <span data-ttu-id="99869-116">Crie um objeto de namespace e carregue seus dados de tipo.</span><span class="sxs-lookup"><span data-stu-id="99869-116">Create a namespace object and load its type data.</span></span>      |
| <span data-ttu-id="99869-117">**CSampleDSNamespace:: createnamespace**</span><span class="sxs-lookup"><span data-stu-id="99869-117">**CSampleDSNamespace::CreateNamespace**</span></span>                  | <span data-ttu-id="99869-118">Aloque, inicialize e valide um objeto de namespace.</span><span class="sxs-lookup"><span data-stu-id="99869-118">Allocate, initialize, and validate a namespace object.</span></span> |
| <span data-ttu-id="99869-119">**CSampleDSNamespace:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="99869-119">**CSampleDSNamespace::QueryInterface**</span></span>                   | <span data-ttu-id="99869-120">Verifique a IID fornecida neste objeto.</span><span class="sxs-lookup"><span data-stu-id="99869-120">Verify the given IID on this object.</span></span>                   |



 

 

 




