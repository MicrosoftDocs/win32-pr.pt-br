---
description: A propriedade Context retorna o contexto deste patch.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Propriedade patch. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747751"
---
# <a name="patchcontext-property"></a><span data-ttu-id="44ca1-103">Propriedade patch. Context</span><span class="sxs-lookup"><span data-stu-id="44ca1-103">Patch.Context property</span></span>

<span data-ttu-id="44ca1-104">A propriedade **Context** retorna o contexto deste patch.</span><span class="sxs-lookup"><span data-stu-id="44ca1-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="44ca1-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="44ca1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ca1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44ca1-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="44ca1-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="44ca1-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="44ca1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="44ca1-108">Remarks</span></span>

<span data-ttu-id="44ca1-109">Essa propriedade retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="44ca1-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="44ca1-110">Contexto</span><span class="sxs-lookup"><span data-stu-id="44ca1-110">Context</span></span>                        | <span data-ttu-id="44ca1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="44ca1-111">Value</span></span> | <span data-ttu-id="44ca1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="44ca1-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="44ca1-113">MSIINSTALLCONTEXT \_ USERmanaged</span><span class="sxs-lookup"><span data-stu-id="44ca1-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="44ca1-114">1</span><span class="sxs-lookup"><span data-stu-id="44ca1-114">1</span></span>     | <span data-ttu-id="44ca1-115">Patch em contexto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="44ca1-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="44ca1-116">\_usuário MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="44ca1-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="44ca1-117">2</span><span class="sxs-lookup"><span data-stu-id="44ca1-117">2</span></span>     | <span data-ttu-id="44ca1-118">Patch em contexto não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="44ca1-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="44ca1-119">\_máquina MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="44ca1-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="44ca1-120">4</span><span class="sxs-lookup"><span data-stu-id="44ca1-120">4</span></span>     | <span data-ttu-id="44ca1-121">Patch no contexto da máquina.</span><span class="sxs-lookup"><span data-stu-id="44ca1-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="44ca1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ca1-122">Requirements</span></span>



| <span data-ttu-id="44ca1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ca1-123">Requirement</span></span> | <span data-ttu-id="44ca1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="44ca1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ca1-125">Versão</span><span class="sxs-lookup"><span data-stu-id="44ca1-125">Version</span></span><br/> | <span data-ttu-id="44ca1-126">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44ca1-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="44ca1-127">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44ca1-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="44ca1-128">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="44ca1-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="44ca1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44ca1-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="44ca1-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ca1-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="44ca1-131">IID</span><span class="sxs-lookup"><span data-stu-id="44ca1-131">IID</span></span><br/>     | <span data-ttu-id="44ca1-132">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="44ca1-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="44ca1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="44ca1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ca1-134">**Objeto patch**</span><span class="sxs-lookup"><span data-stu-id="44ca1-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="44ca1-135">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="44ca1-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




