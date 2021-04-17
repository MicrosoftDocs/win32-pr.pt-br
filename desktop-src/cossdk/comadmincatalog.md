---
description: Acessa os dados armazenados no catálogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457098"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="a78f8-103">Classe COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="a78f8-103">COMAdminCatalog class</span></span>

<span data-ttu-id="a78f8-104">Acessa os dados armazenados no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="a78f8-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a78f8-105">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="a78f8-105">When to implement</span></span>

<span data-ttu-id="a78f8-106">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="a78f8-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a78f8-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="a78f8-107">Requirement</span></span> | <span data-ttu-id="a78f8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a78f8-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a78f8-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="a78f8-109">CLSID</span></span>      | <span data-ttu-id="a78f8-110">\_COMADMINCATALOG CLSID</span><span class="sxs-lookup"><span data-stu-id="a78f8-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="a78f8-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="a78f8-111">ProgID</span></span>     | <span data-ttu-id="a78f8-112">L "COMAdmin. COMAdminCatalog"</span><span class="sxs-lookup"><span data-stu-id="a78f8-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="a78f8-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a78f8-113">Interfaces</span></span> | [<span data-ttu-id="a78f8-114">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="a78f8-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="a78f8-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="a78f8-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="a78f8-116">Quando usar</span><span class="sxs-lookup"><span data-stu-id="a78f8-116">When to use</span></span>

<span data-ttu-id="a78f8-117">Você usa objetos criados a partir da classe **COMAdminCatalog** para iniciar o acesso programático aos dados de configuração com+ armazenados no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="a78f8-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="a78f8-118">Essas informações baseiam-se nas pastas e nos itens na árvore de console da ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a78f8-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="a78f8-119">A classe **COMAdminCatalog** permite que você acesse coleções no catálogo, instale aplicativos e componentes com+, inicie e interrompa os serviços, e conecte-se a servidores remotos e a administre.</span><span class="sxs-lookup"><span data-stu-id="a78f8-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="a78f8-120">As pastas na ferramenta de administração de serviços de componentes correspondem às coleções no catálogo, que você pode representar usando objetos criados na classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a78f8-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="a78f8-121">Os itens nas pastas correspondem aos itens nas coleções, que você pode representar usando objetos criados a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a78f8-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="a78f8-122">Nem todas as coleções e os itens expostos por meio de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) estão disponíveis na ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a78f8-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="a78f8-123">Para obter informações sobre coleções específicas e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a78f8-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="a78f8-124">Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="a78f8-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a78f8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a78f8-125">Remarks</span></span>

<span data-ttu-id="a78f8-126">Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="a78f8-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="a78f8-127">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.</span><span class="sxs-lookup"><span data-stu-id="a78f8-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="a78f8-128">Um objeto COMAdminCatalog pode ser declarado usando "COMAdmin. COMAdminCatalog" como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="a78f8-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="a78f8-129">No COM+ 1,5, lançado com o Windows XP, a classe **COMAdminCatalog** implementa a interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) .</span><span class="sxs-lookup"><span data-stu-id="a78f8-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="a78f8-130">No entanto, no COM+ 1,0, lançado com o Windows 2000, a classe **COMAdminCatalog** implementa apenas a interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="a78f8-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a78f8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a78f8-131">Requirements</span></span>



| <span data-ttu-id="a78f8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a78f8-132">Requirement</span></span> | <span data-ttu-id="a78f8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a78f8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a78f8-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a78f8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a78f8-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a78f8-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a78f8-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a78f8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a78f8-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a78f8-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a78f8-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a78f8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a78f8-139"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a78f8-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="a78f8-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="a78f8-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a78f8-141"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a78f8-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a78f8-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a78f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a78f8-143">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="a78f8-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="a78f8-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="a78f8-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="a78f8-145">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="a78f8-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="a78f8-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="a78f8-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

