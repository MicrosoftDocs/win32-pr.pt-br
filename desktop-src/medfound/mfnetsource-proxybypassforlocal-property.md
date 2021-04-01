---
description: Especifica se o localizador de proxy deve usar um servidor proxy para endereços locais.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Propriedade MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646573"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="a2edd-103">\_Propriedade MFNETSOURCE PROXYBYPASSFORLOCAL</span><span class="sxs-lookup"><span data-stu-id="a2edd-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="a2edd-104">Especifica se o localizador de proxy deve usar um servidor proxy para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="a2edd-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="a2edd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a2edd-105">Data type</span></span>

<span data-ttu-id="a2edd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a2edd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a2edd-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a2edd-107">PROPVARIANT member</span></span>

<span data-ttu-id="a2edd-108">Booliano (**longo**)</span><span class="sxs-lookup"><span data-stu-id="a2edd-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="a2edd-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="a2edd-109">VT\_I4</span></span>

<span data-ttu-id="a2edd-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="a2edd-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a2edd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2edd-111">Remarks</span></span>

<span data-ttu-id="a2edd-112">A constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a2edd-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="a2edd-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="a2edd-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a2edd-114">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="a2edd-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="a2edd-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="a2edd-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="a2edd-116">O valor deve ser definido como 0 se o servidor proxy for usado para endereços locais; caso contrário, um valor diferente de zero configurará o localizador de proxy padrão para ignorar o servidor proxy para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="a2edd-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2edd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2edd-117">Requirements</span></span>



| <span data-ttu-id="a2edd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2edd-118">Requirement</span></span> | <span data-ttu-id="a2edd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a2edd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2edd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2edd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2edd-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2edd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a2edd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2edd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2edd-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2edd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a2edd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2edd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2edd-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2edd-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2edd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2edd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2edd-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2edd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a2edd-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2edd-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a2edd-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="a2edd-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




