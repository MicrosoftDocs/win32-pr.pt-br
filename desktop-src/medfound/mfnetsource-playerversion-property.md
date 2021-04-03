---
description: O valor do campo &\# 0034; c-playerversion&\# 0034; que a fonte de rede usa para o registro em log.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Propriedade MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663211"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="f0078-103">\_Propriedade MFNETSOURCE PLAYERVERSION</span><span class="sxs-lookup"><span data-stu-id="f0078-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="f0078-104">O valor do campo "c-playerversion" usado pela fonte de rede para registro em log.</span><span class="sxs-lookup"><span data-stu-id="f0078-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="f0078-105">Os aplicativos podem definir essa propriedade como o número de versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f0078-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="f0078-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f0078-106">Data type</span></span>

<span data-ttu-id="f0078-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f0078-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f0078-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f0078-108">PROPVARIANT member</span></span>

<span data-ttu-id="f0078-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f0078-109">**LONGLONG**</span></span>

<span data-ttu-id="f0078-110">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="f0078-110">VT\_I8</span></span>

<span data-ttu-id="f0078-111">**hVal**</span><span class="sxs-lookup"><span data-stu-id="f0078-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f0078-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0078-112">Remarks</span></span>

<span data-ttu-id="f0078-113">A constante **MFNETSOURCE \_ PLAYERVERSION** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f0078-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="f0078-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="f0078-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f0078-115">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="f0078-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="f0078-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="f0078-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f0078-117">Para obter mais informações, consulte [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="f0078-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0078-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0078-118">Requirements</span></span>



| <span data-ttu-id="f0078-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0078-119">Requirement</span></span> | <span data-ttu-id="f0078-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f0078-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0078-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0078-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0078-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0078-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0078-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0078-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0078-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0078-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f0078-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0078-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0078-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0078-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0078-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0078-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0078-128">Log de cliente</span><span class="sxs-lookup"><span data-stu-id="f0078-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="f0078-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0078-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f0078-130">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0078-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




