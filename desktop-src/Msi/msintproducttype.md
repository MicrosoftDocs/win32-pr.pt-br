---
description: O instalador define a propriedade MsiNTProductType para sistemas operacionais Windows NT, Windows 2000 e posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriedade MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758953"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="a618a-103">Propriedade MsiNTProductType</span><span class="sxs-lookup"><span data-stu-id="a618a-103">MsiNTProductType property</span></span>

<span data-ttu-id="a618a-104">O instalador define a propriedade **MsiNTProductType** para sistemas operacionais Windows NT, Windows 2000 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="a618a-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="a618a-105">Essa propriedade indica o tipo de produto do Windows.</span><span class="sxs-lookup"><span data-stu-id="a618a-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="a618a-106">Para sistemas operacionais Windows 2000 e posteriores, o instalador define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a618a-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="a618a-107">Observe que os valores são os mesmos do campo **wProductType** da estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a618a-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="a618a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a618a-108">Value</span></span> | <span data-ttu-id="a618a-109">Significado</span><span class="sxs-lookup"><span data-stu-id="a618a-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="a618a-110">1</span><span class="sxs-lookup"><span data-stu-id="a618a-110">1</span></span>     | <span data-ttu-id="a618a-111">Windows 2000 Professional e posterior</span><span class="sxs-lookup"><span data-stu-id="a618a-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="a618a-112">2</span><span class="sxs-lookup"><span data-stu-id="a618a-112">2</span></span>     | <span data-ttu-id="a618a-113">Controlador de domínio do Windows 2000 e posterior</span><span class="sxs-lookup"><span data-stu-id="a618a-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="a618a-114">3</span><span class="sxs-lookup"><span data-stu-id="a618a-114">3</span></span>     | <span data-ttu-id="a618a-115">Windows 2000 Server e posterior</span><span class="sxs-lookup"><span data-stu-id="a618a-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="a618a-116">Para sistemas operacionais anteriores ao Windows 2000, o instalador define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a618a-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="a618a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a618a-117">Value</span></span> | <span data-ttu-id="a618a-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a618a-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="a618a-119">1</span><span class="sxs-lookup"><span data-stu-id="a618a-119">1</span></span>     | <span data-ttu-id="a618a-120">Estação de trabalho do Windows NT</span><span class="sxs-lookup"><span data-stu-id="a618a-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="a618a-121">2</span><span class="sxs-lookup"><span data-stu-id="a618a-121">2</span></span>     | <span data-ttu-id="a618a-122">Controlador de domínio do Windows NT</span><span class="sxs-lookup"><span data-stu-id="a618a-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="a618a-123">3</span><span class="sxs-lookup"><span data-stu-id="a618a-123">3</span></span>     | <span data-ttu-id="a618a-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="a618a-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="a618a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a618a-125">Requirements</span></span>



| <span data-ttu-id="a618a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a618a-126">Requirement</span></span> | <span data-ttu-id="a618a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a618a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a618a-128">Versão</span><span class="sxs-lookup"><span data-stu-id="a618a-128">Version</span></span><br/> | <span data-ttu-id="a618a-129">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a618a-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a618a-130">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a618a-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a618a-131">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a618a-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a618a-132">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a618a-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a618a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a618a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a618a-134">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a618a-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
