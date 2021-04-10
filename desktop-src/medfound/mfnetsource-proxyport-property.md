---
description: Especifica o número da porta do servidor proxy.
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: Propriedade MFNETSOURCE_PROXYPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165011"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="6a3fe-103">\_Propriedade MFNETSOURCE PROXYPORT</span><span class="sxs-lookup"><span data-stu-id="6a3fe-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="6a3fe-104">Especifica o número da porta do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="6a3fe-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="6a3fe-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6a3fe-105">Data type</span></span>

<span data-ttu-id="6a3fe-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6a3fe-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6a3fe-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6a3fe-107">PROPVARIANT member</span></span>

<span data-ttu-id="6a3fe-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="6a3fe-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="6a3fe-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="6a3fe-109">VT\_I4</span></span>

<span data-ttu-id="6a3fe-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="6a3fe-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6a3fe-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a3fe-111">Remarks</span></span>

<span data-ttu-id="6a3fe-112">A constante **MFNETSOURCE \_ PROXYPORT** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6a3fe-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="6a3fe-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="6a3fe-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6a3fe-114">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="6a3fe-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="6a3fe-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="6a3fe-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="6a3fe-116">Se essa propriedade não for definida para HTTP, por padrão, o localizador de proxy usará um valor de 80.</span><span class="sxs-lookup"><span data-stu-id="6a3fe-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a3fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a3fe-117">Requirements</span></span>



| <span data-ttu-id="6a3fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a3fe-118">Requirement</span></span> | <span data-ttu-id="6a3fe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6a3fe-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3fe-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a3fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3fe-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a3fe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a3fe-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a3fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3fe-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a3fe-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a3fe-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a3fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a3fe-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a3fe-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a3fe-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a3fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a3fe-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a3fe-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6a3fe-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a3fe-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6a3fe-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="6a3fe-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




