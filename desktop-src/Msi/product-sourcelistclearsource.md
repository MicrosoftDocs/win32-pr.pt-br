---
description: O método SourceListClearSource remove uma fonte de rede ou URL. Aceita o tipo, o tipo de origem e o SourcePath, o caminho de origem, como parâmetros a serem removidos. Esse método chama o MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Método Product. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747743"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="4b17d-105">Método Product. SourceListClearSource</span><span class="sxs-lookup"><span data-stu-id="4b17d-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="4b17d-106">O método **SourceListClearSource** remove uma fonte de rede ou URL.</span><span class="sxs-lookup"><span data-stu-id="4b17d-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="4b17d-107">Aceita o *tipo*, o tipo de origem e o *SourcePath*, o caminho de origem, como parâmetros a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="4b17d-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="4b17d-108">Esse método chama o [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="4b17d-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b17d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b17d-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="4b17d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b17d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b17d-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="4b17d-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="4b17d-112">Tipo de fonte a ser removida: MSISOURCETYPE \_ rede ou \_ URL de MSISOURCETYPE.</span><span class="sxs-lookup"><span data-stu-id="4b17d-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="4b17d-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="4b17d-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="4b17d-114">Caminho para a origem a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4b17d-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b17d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b17d-115">Return value</span></span>

<span data-ttu-id="4b17d-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b17d-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b17d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b17d-117">Requirements</span></span>



| <span data-ttu-id="4b17d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b17d-118">Requirement</span></span> | <span data-ttu-id="4b17d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4b17d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b17d-120">Versão</span><span class="sxs-lookup"><span data-stu-id="4b17d-120">Version</span></span><br/> | <span data-ttu-id="4b17d-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b17d-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4b17d-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4b17d-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4b17d-123">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4b17d-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="4b17d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4b17d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4b17d-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b17d-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="4b17d-126">IID</span><span class="sxs-lookup"><span data-stu-id="4b17d-126">IID</span></span><br/>     | <span data-ttu-id="4b17d-127">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4b17d-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="4b17d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b17d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b17d-129">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="4b17d-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="4b17d-130">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="4b17d-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="4b17d-131">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4b17d-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




