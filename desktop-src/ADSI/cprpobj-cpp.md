---
title: CPRPOBJ. CPP
description: No componente de provedor de exemplo, os métodos de objeto de propriedade, em cprpobj. cpp, são listados na tabela a seguir.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159302"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="1a626-103">CPRPOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="1a626-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="1a626-104">No componente de provedor de exemplo, os métodos de objeto de propriedade, em cprpobj. cpp, são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a626-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="1a626-105">Método</span><span class="sxs-lookup"><span data-stu-id="1a626-105">Method</span></span>                                                 | <span data-ttu-id="1a626-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a626-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a626-107">**CSampleDSProperty::CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="1a626-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="1a626-108">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="1a626-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="1a626-109">**CSampleDSProperty:: ~ CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="1a626-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="1a626-110">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="1a626-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="1a626-111">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="1a626-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="1a626-112">Crie um objeto de propriedade ADS, pesquisando as definições de atributo chamando **SampleDSGetPropertyDefinition**.</span><span class="sxs-lookup"><span data-stu-id="1a626-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="1a626-113">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="1a626-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="1a626-114">Dada a definição do atributo, crie um objeto de propriedade, definindo a correspondência entre as sintaxes de anúncios com suporte e as sintaxes do provedor.</span><span class="sxs-lookup"><span data-stu-id="1a626-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="1a626-115">**CSampleDSProperty::AllocatePropertyObject**</span><span class="sxs-lookup"><span data-stu-id="1a626-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="1a626-116">Crie um objeto de propriedade e carregue seus dados de tipo.</span><span class="sxs-lookup"><span data-stu-id="1a626-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="1a626-117">**CSampleDSProperty:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="1a626-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="1a626-118">Retorne o ponteiro de interface solicitado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="1a626-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="1a626-119">Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) padrão.</span><span class="sxs-lookup"><span data-stu-id="1a626-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="1a626-120">Métodos [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) padrão.</span><span class="sxs-lookup"><span data-stu-id="1a626-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="1a626-121">**MapSyntaxIdtoADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="1a626-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="1a626-122">Defina a correspondência entre a ID da sintaxe e a sintaxe ADS.</span><span class="sxs-lookup"><span data-stu-id="1a626-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="1a626-123">**MapSyntaxIdtoSampleDSSyntax**</span><span class="sxs-lookup"><span data-stu-id="1a626-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="1a626-124">Defina a correspondência entre a ID da sintaxe e a sintaxe do provedor.</span><span class="sxs-lookup"><span data-stu-id="1a626-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




