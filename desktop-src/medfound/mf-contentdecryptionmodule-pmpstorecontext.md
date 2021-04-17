---
description: Especifica uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM) que usam MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798318"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="33947-103">\_Propriedade MF CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT</span><span class="sxs-lookup"><span data-stu-id="33947-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="33947-104">Especifica uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM) que usam [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span><span class="sxs-lookup"><span data-stu-id="33947-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="33947-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="33947-105">Data type</span></span>

<span data-ttu-id="33947-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="33947-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="33947-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="33947-107">Property GUID</span></span>

<span data-ttu-id="33947-108">**\_CONTENTDECRYPTIONMODULE MF \_ PMPSTORECONTEXT**</span><span class="sxs-lookup"><span data-stu-id="33947-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="33947-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="33947-109">Property value</span></span>

<span data-ttu-id="33947-110">Uma cadeia de caracteres de contexto usada pelas implementações do módulo de descriptografia de conteúdo (CDM).</span><span class="sxs-lookup"><span data-stu-id="33947-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="33947-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="33947-111">Remarks</span></span>

<span data-ttu-id="33947-112">O implementador CDM deve procurar esse valor e passar o valor para o [Construtor MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) usando o nome da propriedade "Windows. Media. Protection. PMPStoreContext".</span><span class="sxs-lookup"><span data-stu-id="33947-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="33947-113">Os aplicativos não devem criar essa propriedade ao chamar [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="33947-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="33947-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33947-114">Requirements</span></span>



| <span data-ttu-id="33947-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33947-115">Requirement</span></span> | <span data-ttu-id="33947-116">Valor</span><span class="sxs-lookup"><span data-stu-id="33947-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33947-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33947-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33947-118">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="33947-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="33947-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33947-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="33947-120"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="33947-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33947-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="33947-121">See also</span></span>

- [<span data-ttu-id="33947-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33947-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="33947-123">MediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="33947-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




