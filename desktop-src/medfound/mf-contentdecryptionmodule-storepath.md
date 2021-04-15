---
description: Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461184"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="44c5e-103">\_Propriedade MF CONTENTDECRYPTIONMODULE \_ caminhodearmazenamento</span><span class="sxs-lookup"><span data-stu-id="44c5e-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="44c5e-104">Especifica um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.</span><span class="sxs-lookup"><span data-stu-id="44c5e-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="44c5e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44c5e-105">Data type</span></span>

<span data-ttu-id="44c5e-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="44c5e-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="44c5e-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="44c5e-107">Property GUID</span></span>

<span data-ttu-id="44c5e-108">**\_CONTENTDECRYPTIONMODULE MF \_ caminhodearmazenamento**</span><span class="sxs-lookup"><span data-stu-id="44c5e-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="44c5e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="44c5e-109">Property value</span></span>

<span data-ttu-id="44c5e-110">Um caminho de arquivo que representa um local de armazenamento que o módulo de descriptografia de conteúdo (CDM) pode usar para inicialização.</span><span class="sxs-lookup"><span data-stu-id="44c5e-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="44c5e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="44c5e-111">Remarks</span></span>

<span data-ttu-id="44c5e-112">O caminho especificado com essa propriedade também será usado para dados específicos de conteúdo se a propriedade [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="44c5e-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="44c5e-113">Para melhorar o desempenho COM, o aplicativo não deve excluir o local do repositório após o lançamento do objeto CDM.</span><span class="sxs-lookup"><span data-stu-id="44c5e-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="44c5e-114">Defina essa propriedade ao criar um CDM chamando [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="44c5e-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="44c5e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44c5e-115">Requirements</span></span>



| <span data-ttu-id="44c5e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44c5e-116">Requirement</span></span> | <span data-ttu-id="44c5e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44c5e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44c5e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44c5e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44c5e-119">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="44c5e-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="44c5e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44c5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44c5e-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="44c5e-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c5e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="44c5e-122">See also</span></span>

- [<span data-ttu-id="44c5e-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44c5e-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="44c5e-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="44c5e-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




