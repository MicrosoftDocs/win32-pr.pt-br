---
description: A propriedade State retorna o estado de instalação dessa instância do patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Propriedade patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751430"
---
# <a name="patchstate-property"></a><span data-ttu-id="bfdff-103">Propriedade patch. State</span><span class="sxs-lookup"><span data-stu-id="bfdff-103">Patch.State property</span></span>

<span data-ttu-id="bfdff-104">A propriedade **State** retorna o estado de instalação dessa instância do patch.</span><span class="sxs-lookup"><span data-stu-id="bfdff-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="bfdff-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bfdff-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdff-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfdff-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="bfdff-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bfdff-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bfdff-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfdff-108">Remarks</span></span>

<span data-ttu-id="bfdff-109">Essa propriedade retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfdff-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="bfdff-110">Estado da instalação</span><span class="sxs-lookup"><span data-stu-id="bfdff-110">Installation State</span></span>        | <span data-ttu-id="bfdff-111">Significado</span><span class="sxs-lookup"><span data-stu-id="bfdff-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bfdff-112">MSIPATCHSTATE \_ aplicado</span><span class="sxs-lookup"><span data-stu-id="bfdff-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="bfdff-113">O patch é aplicado a esta instância de produto.</span><span class="sxs-lookup"><span data-stu-id="bfdff-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="bfdff-114">MSIPATCHSTATE \_ substituído</span><span class="sxs-lookup"><span data-stu-id="bfdff-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="bfdff-115">O patch é aplicado a esta instância do produto, mas está substituído.</span><span class="sxs-lookup"><span data-stu-id="bfdff-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="bfdff-116">MSIPATCHSTATE \_ obsoleto</span><span class="sxs-lookup"><span data-stu-id="bfdff-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="bfdff-117">O patch é aplicado nesta instância do produto, mas obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bfdff-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="bfdff-118">Esse método pode retornar \_ um patch desconhecido de erro \_ , se o objeto [**patch**](patch-object.md) for inicializado com uma cadeia de caracteres vazia para *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="bfdff-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfdff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfdff-119">Requirements</span></span>



| <span data-ttu-id="bfdff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfdff-120">Requirement</span></span> | <span data-ttu-id="bfdff-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bfdff-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdff-122">Versão</span><span class="sxs-lookup"><span data-stu-id="bfdff-122">Version</span></span><br/> | <span data-ttu-id="bfdff-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bfdff-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bfdff-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bfdff-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bfdff-125">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bfdff-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="bfdff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bfdff-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="bfdff-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfdff-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="bfdff-128">IID</span><span class="sxs-lookup"><span data-stu-id="bfdff-128">IID</span></span><br/>     | <span data-ttu-id="bfdff-129">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bfdff-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="bfdff-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfdff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdff-131">**Patch**</span><span class="sxs-lookup"><span data-stu-id="bfdff-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="bfdff-132">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="bfdff-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="bfdff-133">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="bfdff-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




