---
description: Habilita ou desabilita o modo de visualização, o que permite que o aplicativo substitua a lógica de buffer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Propriedade MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749957"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="dff8b-103">\_Propriedade MFNETSOURCE PREVIEWMODEENABLED</span><span class="sxs-lookup"><span data-stu-id="dff8b-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="dff8b-104">Habilita ou desabilita o modo de visualização, o que permite que o aplicativo substitua a lógica de buffer inicial.</span><span class="sxs-lookup"><span data-stu-id="dff8b-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="dff8b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dff8b-105">Data type</span></span>

<span data-ttu-id="dff8b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="dff8b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="dff8b-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="dff8b-107">PROPVARIANT member</span></span>

<span data-ttu-id="dff8b-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="dff8b-108">**BOOL**</span></span>

<span data-ttu-id="dff8b-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="dff8b-109">VT\_BOOL</span></span>

<span data-ttu-id="dff8b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="dff8b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="dff8b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dff8b-111">Remarks</span></span>

<span data-ttu-id="dff8b-112">A constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dff8b-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="dff8b-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="dff8b-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="dff8b-114">Essa propriedade é definida na fonte de rede passando um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="dff8b-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="dff8b-115">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="dff8b-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dff8b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dff8b-116">Requirements</span></span>



| <span data-ttu-id="dff8b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff8b-117">Requirement</span></span> | <span data-ttu-id="dff8b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dff8b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dff8b-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dff8b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dff8b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dff8b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="dff8b-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="dff8b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dff8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff8b-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff8b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff8b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dff8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff8b-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dff8b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dff8b-127">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dff8b-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




