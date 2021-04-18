---
description: Quantidade máxima de dados que os buffers de origem de rede, em milissegundos.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Propriedade MFNETSOURCE_MAXBUFFERTIMEMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788939"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="becea-103">\_Propriedade MFNETSOURCE MAXBUFFERTIMEMS</span><span class="sxs-lookup"><span data-stu-id="becea-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="becea-104">Quantidade máxima de dados que os buffers de origem de rede, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="becea-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="becea-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="becea-105">Data type</span></span>

<span data-ttu-id="becea-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="becea-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="becea-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="becea-107">PROPVARIANT member</span></span>

<span data-ttu-id="becea-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="becea-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="becea-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="becea-109">VT\_I4</span></span>

<span data-ttu-id="becea-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="becea-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="becea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="becea-111">Remarks</span></span>

<span data-ttu-id="becea-112">A constante **MFNETSOURCE \_ MAXBUFFERTIMEMS** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="becea-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="becea-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="becea-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="becea-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="becea-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="becea-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="becea-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="becea-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="becea-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="becea-117">O valor padrão dessa propriedade é 40.000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="becea-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="becea-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="becea-118">Requirements</span></span>



| <span data-ttu-id="becea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="becea-119">Requirement</span></span> | <span data-ttu-id="becea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="becea-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="becea-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="becea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="becea-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="becea-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="becea-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="becea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="becea-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="becea-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="becea-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="becea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="becea-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="becea-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="becea-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="becea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="becea-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="becea-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="becea-129">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="becea-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="becea-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="becea-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




