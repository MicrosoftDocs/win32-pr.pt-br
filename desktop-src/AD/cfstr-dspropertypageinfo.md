---
title: CFSTR_DSPROPERTYPAGEINFO (DSClient. h)
description: O \_ formato de área de transferência CFSTR DSPROPERTYPAGEINFO fornece um HGLOBAL que contém uma estrutura DSPROPERTYPAGEINFO.
ms.assetid: 84ed1322-fee3-44ee-873e-57586261ff62
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSPROPERTYPAGEINFO
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259c9addbb3ee41c7b12cd7ea77eb8393b69daaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009210"
---
# <a name="cfstr_dspropertypageinfo"></a><span data-ttu-id="21aaf-103">CFSTR \_ DSPROPERTYPAGEINFO</span><span class="sxs-lookup"><span data-stu-id="21aaf-103">CFSTR\_DSPROPERTYPAGEINFO</span></span>

<dl> <dt>

<span data-ttu-id="21aaf-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR \_ DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="21aaf-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR\_DSPROPERTYPAGEINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21aaf-105">"DsPropPageInfo"</span><span class="sxs-lookup"><span data-stu-id="21aaf-105">"DsPropPageInfo"</span></span>
</dt> <dt>



<span data-ttu-id="21aaf-106">O formato de área de transferência **CFSTR \_ DSPROPERTYPAGEINFO** fornece um **HGLOBAL** que contém uma estrutura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) .</span><span class="sxs-lookup"><span data-stu-id="21aaf-106">The **CFSTR\_DSPROPERTYPAGEINFO** clipboard format provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure.</span></span> <span data-ttu-id="21aaf-107">A estrutura **DSPROPERTYPAGEINFO** contém a cadeia de caracteres opcional que a extensão adicionou aos valores de parâmetro **adminPropertySheet** e/ou **shellPropertySheet** quando a extensão foi registrada.</span><span class="sxs-lookup"><span data-stu-id="21aaf-107">The **DSPROPERTYPAGEINFO** structure contains the optional string that the extension added to the **adminPropertySheet** and/or **shellPropertySheet** parameter values when the extension was registered.</span></span> <span data-ttu-id="21aaf-108">Para obter mais informações sobre como essa cadeia de caracteres é definida, consulte [registrando o objeto com da página de propriedades em um especificador de exibição](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="21aaf-108">For more information about how this string is set, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21aaf-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21aaf-109">Requirements</span></span>



| <span data-ttu-id="21aaf-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="21aaf-110">Requirement</span></span> | <span data-ttu-id="21aaf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="21aaf-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21aaf-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21aaf-112">Minimum supported client</span></span><br/> | <span data-ttu-id="21aaf-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21aaf-113">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="21aaf-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21aaf-114">Minimum supported server</span></span><br/> | <span data-ttu-id="21aaf-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21aaf-115">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="21aaf-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21aaf-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="21aaf-117"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="21aaf-117"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21aaf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="21aaf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21aaf-119">**DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="21aaf-119">**DSPROPERTYPAGEINFO**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo)
</dt> <dt>

[<span data-ttu-id="21aaf-120">Registrando o objeto COM da página de propriedades em um especificador de exibição</span><span class="sxs-lookup"><span data-stu-id="21aaf-120">Registering the Property Page COM Object in a Display Specifier</span></span>](registering-the-property-page-com-object-in-a-display-specifier.md)
</dt> </dl>

 

 





