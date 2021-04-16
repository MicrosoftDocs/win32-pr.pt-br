---
description: A propriedade Context retorna o contexto deste produto.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Propriedade Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751429"
---
# <a name="productcontext-property"></a><span data-ttu-id="f978c-103">Propriedade Product. Context</span><span class="sxs-lookup"><span data-stu-id="f978c-103">Product.Context property</span></span>

<span data-ttu-id="f978c-104">A propriedade **Context** retorna o contexto deste produto.</span><span class="sxs-lookup"><span data-stu-id="f978c-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="f978c-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f978c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f978c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f978c-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="f978c-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f978c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f978c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f978c-108">Remarks</span></span>

<span data-ttu-id="f978c-109">Essa propriedade pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f978c-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="f978c-110">Contexto</span><span class="sxs-lookup"><span data-stu-id="f978c-110">Context</span></span>                        | <span data-ttu-id="f978c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f978c-111">Value</span></span> | <span data-ttu-id="f978c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f978c-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="f978c-113">MSIINSTALLCONTEXT \_ USERmanaged</span><span class="sxs-lookup"><span data-stu-id="f978c-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="f978c-114">1</span><span class="sxs-lookup"><span data-stu-id="f978c-114">1</span></span>     | <span data-ttu-id="f978c-115">Produtos sob contexto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f978c-115">Products under managed context.</span></span>   |
| <span data-ttu-id="f978c-116">\_usuário MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="f978c-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="f978c-117">2</span><span class="sxs-lookup"><span data-stu-id="f978c-117">2</span></span>     | <span data-ttu-id="f978c-118">Produtos sob contexto não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f978c-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="f978c-119">\_máquina MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="f978c-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="f978c-120">4</span><span class="sxs-lookup"><span data-stu-id="f978c-120">4</span></span>     | <span data-ttu-id="f978c-121">Produtos sob o contexto do computador.</span><span class="sxs-lookup"><span data-stu-id="f978c-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="f978c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f978c-122">Requirements</span></span>



| <span data-ttu-id="f978c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f978c-123">Requirement</span></span> | <span data-ttu-id="f978c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f978c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f978c-125">Versão</span><span class="sxs-lookup"><span data-stu-id="f978c-125">Version</span></span><br/> | <span data-ttu-id="f978c-126">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f978c-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f978c-127">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f978c-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f978c-128">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f978c-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f978c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f978c-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f978c-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f978c-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f978c-131">IID</span><span class="sxs-lookup"><span data-stu-id="f978c-131">IID</span></span><br/>     | <span data-ttu-id="f978c-132">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f978c-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="f978c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f978c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f978c-134">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="f978c-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="f978c-135">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="f978c-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




