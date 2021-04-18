---
description: Especifica uma política de controle de plug-in local.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Atributo MF_LOCAL_PLUGIN_CONTROL_POLICY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751975"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="cab19-103">\_Atributo de \_ política de controle de plug-in local MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="cab19-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="cab19-104">Especifica uma política de controle de plug-in local.</span><span class="sxs-lookup"><span data-stu-id="cab19-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="cab19-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cab19-105">Data type</span></span>

<span data-ttu-id="cab19-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cab19-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cab19-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cab19-107">Remarks</span></span>

<span data-ttu-id="cab19-108">Defina esse atributo como um dos valores [**da \_ \_ \_ política de controle do plug-in MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .</span><span class="sxs-lookup"><span data-stu-id="cab19-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="cab19-109">Esses atributos permitem que o aplicativo especifique uma política local mais restritiva do que a política de todo o processo configurada pelo [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span><span class="sxs-lookup"><span data-stu-id="cab19-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="cab19-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cab19-110">Requirements</span></span>



| <span data-ttu-id="cab19-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab19-111">Requirement</span></span> | <span data-ttu-id="cab19-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cab19-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cab19-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cab19-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cab19-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cab19-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cab19-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cab19-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cab19-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cab19-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cab19-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cab19-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab19-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab19-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab19-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cab19-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab19-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cab19-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cab19-121">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="cab19-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




