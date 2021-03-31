---
title: Constantes ADSI
description: A tabela a seguir lista as constantes definidas e usadas nas interfaces de serviço do Active Directory (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634897"
---
# <a name="adsi-constants"></a><span data-ttu-id="94bc2-109">Constantes ADSI</span><span class="sxs-lookup"><span data-stu-id="94bc2-109">ADSI Constants</span></span>

<span data-ttu-id="94bc2-110">A tabela a seguir lista as constantes definidas e usadas nas interfaces de serviço do Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="94bc2-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="94bc2-111">Constante de ADSI</span><span class="sxs-lookup"><span data-stu-id="94bc2-111">ADSI constant</span></span>                      | <span data-ttu-id="94bc2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="94bc2-112">Value</span></span>                                   | <span data-ttu-id="94bc2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="94bc2-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94bc2-114">**\_INITCREDENTIALS ext \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="94bc2-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="94bc2-115">1</span><span class="sxs-lookup"><span data-stu-id="94bc2-115">1</span></span>                                       | <span data-ttu-id="94bc2-116">Um código de controle que indica que os dados personalizados fornecidos para o método [**IADsExtension:: opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contêm credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="94bc2-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="94bc2-117">**inicialização de ext de anúncios \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="94bc2-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="94bc2-118">2</span><span class="sxs-lookup"><span data-stu-id="94bc2-118">2</span></span>                                       | <span data-ttu-id="94bc2-119">Um código de controle usado com [**IADsExtension:: Opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que as extensões podem executar qualquer inicialização necessária, dependendo dos recursos com suporte pelo objeto pai.</span><span class="sxs-lookup"><span data-stu-id="94bc2-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="94bc2-120">**\_MAXEXTDISPID ext \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="94bc2-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="94bc2-121">16777215</span><span class="sxs-lookup"><span data-stu-id="94bc2-121">16777215</span></span>                                | <span data-ttu-id="94bc2-122">O DISPID mais alto que um objeto de extensão pode usar para seus métodos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="94bc2-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="94bc2-123">**\_MINEXTDISPID ext \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="94bc2-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="94bc2-124">1</span><span class="sxs-lookup"><span data-stu-id="94bc2-124">1</span></span>                                       | <span data-ttu-id="94bc2-125">O DISPID mais baixo que um objeto de extensão pode usar para seus métodos e propriedades.</span><span class="sxs-lookup"><span data-stu-id="94bc2-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="94bc2-126">**\_resposta VLV de anúncios \_**</span><span class="sxs-lookup"><span data-stu-id="94bc2-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="94bc2-127">L "fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="94bc2-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="94bc2-128">Usado com o método [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar os metadados de pesquisa VLV.</span><span class="sxs-lookup"><span data-stu-id="94bc2-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="94bc2-129">Para obter mais informações, consulte [como Pesquisar usando a VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="94bc2-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="94bc2-130">**DBPROPFLAGS \_ ADSISEARCH**</span><span class="sxs-lookup"><span data-stu-id="94bc2-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="94bc2-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="94bc2-131">0x0000C000</span></span>                              | <span data-ttu-id="94bc2-132">Usado para trabalhar com o provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="94bc2-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




