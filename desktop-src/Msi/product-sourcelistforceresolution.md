---
description: O método SourceListForceResolution limpa a propriedade LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Método Product. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751186"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="21724-103">Método Product. SourceListForceResolution</span><span class="sxs-lookup"><span data-stu-id="21724-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="21724-104">O método **SourceListForceResolution** limpa a propriedade LastUsedSource.</span><span class="sxs-lookup"><span data-stu-id="21724-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="21724-105">Isso forçará o instalador a Pesquisar a lista de origem em busca de uma fonte de produto válida na próxima vez que uma fonte for necessária, como quando o instalador executar uma instalação ou reinstalação, ou quando o caminho for necessário para que um conjunto de componentes seja executado da origem.</span><span class="sxs-lookup"><span data-stu-id="21724-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="21724-106">Esse método chama [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="21724-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="21724-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21724-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="21724-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21724-108">Parameters</span></span>

<span data-ttu-id="21724-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="21724-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21724-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21724-110">Return value</span></span>

<span data-ttu-id="21724-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="21724-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21724-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21724-112">Requirements</span></span>



| <span data-ttu-id="21724-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="21724-113">Requirement</span></span> | <span data-ttu-id="21724-114">Valor</span><span class="sxs-lookup"><span data-stu-id="21724-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21724-115">Versão</span><span class="sxs-lookup"><span data-stu-id="21724-115">Version</span></span><br/> | <span data-ttu-id="21724-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21724-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="21724-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21724-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="21724-118">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="21724-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="21724-119">DLL</span><span class="sxs-lookup"><span data-stu-id="21724-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="21724-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21724-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="21724-121">IID</span><span class="sxs-lookup"><span data-stu-id="21724-121">IID</span></span><br/>     | <span data-ttu-id="21724-122">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="21724-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="21724-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="21724-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21724-124">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="21724-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="21724-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="21724-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="21724-126">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="21724-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




