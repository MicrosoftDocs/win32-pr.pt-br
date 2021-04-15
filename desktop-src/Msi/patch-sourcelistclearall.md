---
description: O método SourceListClearAll do objeto patch limpa a lista de origem completa de todas as fontes do tipo especificado para um patch. Aceita o tipo como um parâmetro. Esse método chama MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Método patch. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752246"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="6cb4b-105">Método patch. SourceListClearAll</span><span class="sxs-lookup"><span data-stu-id="6cb4b-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="6cb4b-106">O método **SourceListClearAll** do objeto [**patch**](patch-object.md) limpa a lista de origem completa de todas as fontes do tipo especificado para um patch.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="6cb4b-107">Aceita o *tipo* como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="6cb4b-108">Esse método chama [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span><span class="sxs-lookup"><span data-stu-id="6cb4b-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb4b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cb4b-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="6cb4b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cb4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb4b-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="6cb4b-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb4b-112">O tipo de tipo de fonte, como rede, URL ou mídia.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb4b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cb4b-113">Return value</span></span>

<span data-ttu-id="6cb4b-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb4b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb4b-115">Requirements</span></span>



| <span data-ttu-id="6cb4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb4b-116">Requirement</span></span> | <span data-ttu-id="6cb4b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb4b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb4b-118">Versão</span><span class="sxs-lookup"><span data-stu-id="6cb4b-118">Version</span></span><br/> | <span data-ttu-id="6cb4b-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6cb4b-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6cb4b-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6cb4b-121">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6cb4b-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6cb4b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6cb4b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6cb4b-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cb4b-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6cb4b-124">IID</span><span class="sxs-lookup"><span data-stu-id="6cb4b-124">IID</span></span><br/>     | <span data-ttu-id="6cb4b-125">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6cb4b-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6cb4b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cb4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb4b-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="6cb4b-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="6cb4b-128">**MsiSourceListClearAllEx**</span><span class="sxs-lookup"><span data-stu-id="6cb4b-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="6cb4b-129">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="6cb4b-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




