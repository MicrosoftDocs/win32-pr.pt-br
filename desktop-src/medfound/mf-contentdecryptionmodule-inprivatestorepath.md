---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501938"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="f69a3-103">\_Propriedade MF CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH</span><span class="sxs-lookup"><span data-stu-id="f69a3-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="f69a3-104">Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f69a3-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="f69a3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f69a3-105">Data type</span></span>

<span data-ttu-id="f69a3-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="f69a3-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f69a3-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="f69a3-107">Property GUID</span></span>

<span data-ttu-id="f69a3-108">**\_CONTENTDECRYPTIONMODULE MF \_ INPRIVATESTOREPATH**</span><span class="sxs-lookup"><span data-stu-id="f69a3-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="f69a3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f69a3-109">Property value</span></span>

<span data-ttu-id="f69a3-110">Um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para dados específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f69a3-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="f69a3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f69a3-111">Remarks</span></span>

<span data-ttu-id="f69a3-112">O aplicativo deve excluir o local do repositório após o lançamento do objeto CDM.</span><span class="sxs-lookup"><span data-stu-id="f69a3-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="f69a3-113">Se essa propriedade não estiver definida, o sistema usará o caminho especificado com a propriedade [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) para dados específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f69a3-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="f69a3-114">Defina essa propriedade ao criar um CDM chamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="f69a3-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="f69a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f69a3-115">Requirements</span></span>



| <span data-ttu-id="f69a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69a3-116">Requirement</span></span> | <span data-ttu-id="f69a3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f69a3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f69a3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f69a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f69a3-119">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f69a3-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="f69a3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f69a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f69a3-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69a3-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69a3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f69a3-122">See also</span></span>

- [<span data-ttu-id="f69a3-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f69a3-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="f69a3-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="f69a3-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




