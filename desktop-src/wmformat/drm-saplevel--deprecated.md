---
title: DRM_SAPLEVEL (preterido)
description: Especifica o nível de caminho de áudio seguro (SAP) com suporte do seu aplicativo.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (preterido) formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751768"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="2b721-104">\_SAPLEVEL DRM (preterido)</span><span class="sxs-lookup"><span data-stu-id="2b721-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="2b721-105">\[**DRM \_ O SAPLEVEL** não está mais disponível para uso a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2b721-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="2b721-106">Em vez disso, use o PUMA (áudio do modo de usuário protegido) na biblioteca Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2b721-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="2b721-107">\]</span><span class="sxs-lookup"><span data-stu-id="2b721-107">\]</span></span>

<span data-ttu-id="2b721-108">A propriedade **DRM \_ SAPLEVEL** especifica o nível de caminho de áudio seguro (SAP) com suporte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b721-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2b721-109">Constante global</span><span class="sxs-lookup"><span data-stu-id="2b721-109">Global Constant</span></span>

<span data-ttu-id="2b721-110">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="2b721-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="2b721-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="2b721-111">Data Type</span></span>

<span data-ttu-id="2b721-112">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="2b721-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="2b721-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b721-113">Remarks</span></span>

<span data-ttu-id="2b721-114">Essa é uma propriedade somente gravação que é definida chamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="2b721-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="2b721-115">O valor é uma representação de cadeia de caracteres de caracteres largos do nível do SAP, como L "200".</span><span class="sxs-lookup"><span data-stu-id="2b721-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="2b721-116">Os valores atuais com suporte são 200 e 300.</span><span class="sxs-lookup"><span data-stu-id="2b721-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b721-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b721-117">Requirements</span></span>



| <span data-ttu-id="2b721-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b721-118">Requirement</span></span> | <span data-ttu-id="2b721-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2b721-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="2b721-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2b721-120">End of client support</span></span><br/> | <span data-ttu-id="2b721-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b721-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="2b721-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2b721-122">End of server support</span></span><br/> | <span data-ttu-id="2b721-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b721-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b721-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b721-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b721-125">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="2b721-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





