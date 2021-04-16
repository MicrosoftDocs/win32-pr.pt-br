---
description: O método SourceListClearAll o objeto Product remove todas as fontes do produto. O tipo de fonte a ser removida pode ser especificado.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Método Product. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749989"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="a09fe-104">Método Product. SourceListClearAll</span><span class="sxs-lookup"><span data-stu-id="a09fe-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="a09fe-105">O método **SourceListClearAll** o objeto [**Product**](product-object.md) remove todas as fontes do produto.</span><span class="sxs-lookup"><span data-stu-id="a09fe-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="a09fe-106">O tipo de fonte a ser removida pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a09fe-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09fe-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="a09fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09fe-109">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="a09fe-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="a09fe-110">Tipo de fonte a ser removida: MSISOURCETYPE \_ Media, MSISOURCETYPE \_ Network ou MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="a09fe-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a09fe-111">Return value</span></span>

<span data-ttu-id="a09fe-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a09fe-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a09fe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09fe-113">Requirements</span></span>



| <span data-ttu-id="a09fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09fe-114">Requirement</span></span> | <span data-ttu-id="a09fe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a09fe-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09fe-116">Versão</span><span class="sxs-lookup"><span data-stu-id="a09fe-116">Version</span></span><br/> | <span data-ttu-id="a09fe-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a09fe-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a09fe-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a09fe-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a09fe-119">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a09fe-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a09fe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a09fe-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a09fe-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a09fe-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a09fe-122">IID</span><span class="sxs-lookup"><span data-stu-id="a09fe-122">IID</span></span><br/>     | <span data-ttu-id="a09fe-123">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a09fe-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="a09fe-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a09fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09fe-125">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="a09fe-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="a09fe-126">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="a09fe-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="a09fe-127">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="a09fe-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




