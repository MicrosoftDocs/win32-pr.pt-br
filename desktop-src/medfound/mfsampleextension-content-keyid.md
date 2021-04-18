---
description: Define a ID da chave para o exemplo.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Atributo MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756523"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="e4a5b-103">\_Atributo keyid de conteúdo MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="e4a5b-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="e4a5b-104">Define a ID da chave para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e4a5b-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4a5b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e4a5b-105">Data type</span></span>

<span data-ttu-id="e4a5b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e4a5b-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="e4a5b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4a5b-107">Examples</span></span>

<span data-ttu-id="e4a5b-108">O exemplo a seguir mostra como definir a ID da chave para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e4a5b-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="e4a5b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4a5b-109">Requirements</span></span>



| <span data-ttu-id="e4a5b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a5b-110">Requirement</span></span> | <span data-ttu-id="e4a5b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e4a5b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a5b-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a5b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a5b-113">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e4a5b-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="e4a5b-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a5b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a5b-115">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e4a5b-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e4a5b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4a5b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a5b-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a5b-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4a5b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4a5b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a5b-119">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4a5b-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e4a5b-120">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e4a5b-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="e4a5b-121">MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit</span><span class="sxs-lookup"><span data-stu-id="e4a5b-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




