---
description: A propriedade State retorna o estado de instalação dessa instância do produto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propriedade Product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751185"
---
# <a name="productstate-property"></a><span data-ttu-id="82174-103">Propriedade Product. State</span><span class="sxs-lookup"><span data-stu-id="82174-103">Product.State property</span></span>

<span data-ttu-id="82174-104">A propriedade **State** retorna o estado de instalação dessa instância do produto.</span><span class="sxs-lookup"><span data-stu-id="82174-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="82174-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="82174-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82174-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82174-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="82174-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="82174-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="82174-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="82174-108">Remarks</span></span>

<span data-ttu-id="82174-109">Essa propriedade retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="82174-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="82174-110">Estado da instalação</span><span class="sxs-lookup"><span data-stu-id="82174-110">Installation State</span></span>       | <span data-ttu-id="82174-111">Significado</span><span class="sxs-lookup"><span data-stu-id="82174-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="82174-112">padrão INSTALLstate \_</span><span class="sxs-lookup"><span data-stu-id="82174-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="82174-113">Instância do produto instalada localmente.</span><span class="sxs-lookup"><span data-stu-id="82174-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="82174-114">INSTALLstate \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="82174-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="82174-115">Instância do produto anunciada.</span><span class="sxs-lookup"><span data-stu-id="82174-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="82174-116">INSTALLstate \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="82174-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="82174-117">Instância do produto desconhecida.</span><span class="sxs-lookup"><span data-stu-id="82174-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="82174-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82174-118">Requirements</span></span>



| <span data-ttu-id="82174-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="82174-119">Requirement</span></span> | <span data-ttu-id="82174-120">Valor</span><span class="sxs-lookup"><span data-stu-id="82174-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82174-121">Versão</span><span class="sxs-lookup"><span data-stu-id="82174-121">Version</span></span><br/> | <span data-ttu-id="82174-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82174-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82174-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82174-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82174-124">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="82174-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="82174-125">DLL</span><span class="sxs-lookup"><span data-stu-id="82174-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="82174-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82174-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="82174-127">IID</span><span class="sxs-lookup"><span data-stu-id="82174-127">IID</span></span><br/>     | <span data-ttu-id="82174-128">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82174-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="82174-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="82174-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82174-130">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="82174-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="82174-131">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="82174-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




