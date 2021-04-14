---
description: Especifica se o localizador de proxy padrão deve forçar a detecção automática de proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: Propriedade MFNETSOURCE_PROXYRERUNAUTODETECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502380"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="a6d9c-103">\_Propriedade MFNETSOURCE PROXYRERUNAUTODETECTION</span><span class="sxs-lookup"><span data-stu-id="a6d9c-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="a6d9c-104">Especifica se o localizador de proxy padrão deve forçar a detecção automática de proxy.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="a6d9c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a6d9c-105">Data type</span></span>

<span data-ttu-id="a6d9c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a6d9c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a6d9c-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a6d9c-107">PROPVARIANT member</span></span>

<span data-ttu-id="a6d9c-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="a6d9c-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="a6d9c-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="a6d9c-109">VT\_I4</span></span>

<span data-ttu-id="a6d9c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="a6d9c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a6d9c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6d9c-111">Remarks</span></span>

<span data-ttu-id="a6d9c-112">A constante **MFNETSOURCE \_ PROXYSETTINGS** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="a6d9c-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a6d9c-114">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="a6d9c-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="a6d9c-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="a6d9c-116">No modo de detecção automática, o localizador de proxy usa o mecanismo de detecção de proxy do WinInet.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="a6d9c-117">Para forçar a detecção automática, defina o valor como 0.</span><span class="sxs-lookup"><span data-stu-id="a6d9c-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d9c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6d9c-118">Requirements</span></span>



| <span data-ttu-id="a6d9c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6d9c-119">Requirement</span></span> | <span data-ttu-id="a6d9c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6d9c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d9c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6d9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d9c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6d9c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6d9c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6d9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d9c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6d9c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6d9c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6d9c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6d9c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d9c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d9c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6d9c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d9c-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6d9c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a6d9c-129">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6d9c-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a6d9c-130">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="a6d9c-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




