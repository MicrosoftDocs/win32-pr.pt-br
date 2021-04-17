---
description: O instalador define a propriedade Productstate como o estado de instalação do produto na inicialização.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propriedade productstate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759379"
---
# <a name="productstate-property"></a><span data-ttu-id="23e77-103">Propriedade productstate</span><span class="sxs-lookup"><span data-stu-id="23e77-103">ProductState property</span></span>

<span data-ttu-id="23e77-104">O instalador define a propriedade **productstate** como o estado de instalação do produto na inicialização.</span><span class="sxs-lookup"><span data-stu-id="23e77-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="23e77-105">Essa propriedade é definida como um dos seguintes tipos de dados INSTALLstate retornados por [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span><span class="sxs-lookup"><span data-stu-id="23e77-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="23e77-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="23e77-106">INSTALLSTATE</span></span>             | <span data-ttu-id="23e77-107">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="23e77-107">Numeric value</span></span> | <span data-ttu-id="23e77-108">Estado de instalação do produto</span><span class="sxs-lookup"><span data-stu-id="23e77-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="23e77-109">INSTALLstate \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="23e77-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="23e77-110">-1</span><span class="sxs-lookup"><span data-stu-id="23e77-110">-1</span></span>            | <span data-ttu-id="23e77-111">O produto não é anunciado nem instalado.</span><span class="sxs-lookup"><span data-stu-id="23e77-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="23e77-112">INSTALLstate \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="23e77-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="23e77-113">1</span><span class="sxs-lookup"><span data-stu-id="23e77-113">1</span></span>             | <span data-ttu-id="23e77-114">O produto é anunciado, mas não está instalado.</span><span class="sxs-lookup"><span data-stu-id="23e77-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="23e77-115">INSTALLstate \_ ausente</span><span class="sxs-lookup"><span data-stu-id="23e77-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="23e77-116">2</span><span class="sxs-lookup"><span data-stu-id="23e77-116">2</span></span>             | <span data-ttu-id="23e77-117">O produto está instalado para um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="23e77-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="23e77-118">padrão INSTALLstate \_</span><span class="sxs-lookup"><span data-stu-id="23e77-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="23e77-119">5</span><span class="sxs-lookup"><span data-stu-id="23e77-119">5</span></span>             | <span data-ttu-id="23e77-120">O produto está instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="23e77-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="23e77-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23e77-121">Requirements</span></span>



| <span data-ttu-id="23e77-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e77-122">Requirement</span></span> | <span data-ttu-id="23e77-123">Valor</span><span class="sxs-lookup"><span data-stu-id="23e77-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e77-124">Versão</span><span class="sxs-lookup"><span data-stu-id="23e77-124">Version</span></span><br/> | <span data-ttu-id="23e77-125">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23e77-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="23e77-126">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="23e77-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="23e77-127">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23e77-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="23e77-128">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="23e77-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23e77-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="23e77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e77-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="23e77-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




