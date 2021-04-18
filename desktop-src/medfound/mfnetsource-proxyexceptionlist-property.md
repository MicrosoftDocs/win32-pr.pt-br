---
description: Especifica uma lista delimitada por ponto-e-vírgula dos servidores de mídia que podem aceitar conexões de aplicativos cliente sem usar um servidor proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: Propriedade MFNETSOURCE_PROXYEXCEPTIONLIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814458"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="e11f1-103">\_Propriedade MFNETSOURCE PROXYEXCEPTIONLIST</span><span class="sxs-lookup"><span data-stu-id="e11f1-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="e11f1-104">Especifica uma lista delimitada por ponto-e-vírgula dos servidores de mídia que podem aceitar conexões de aplicativos cliente sem usar um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="e11f1-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="e11f1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e11f1-105">Data type</span></span>

<span data-ttu-id="e11f1-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e11f1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e11f1-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e11f1-107">PROPVARIANT member</span></span>

<span data-ttu-id="e11f1-108">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="e11f1-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="e11f1-109">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="e11f1-109">VT\_LPWSTR</span></span>

<span data-ttu-id="e11f1-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="e11f1-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e11f1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e11f1-111">Remarks</span></span>

<span data-ttu-id="e11f1-112">A constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e11f1-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="e11f1-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="e11f1-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e11f1-114">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="e11f1-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="e11f1-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="e11f1-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="e11f1-116">O localizador de proxy não executa a detecção de proxy para esses endereços.</span><span class="sxs-lookup"><span data-stu-id="e11f1-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11f1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11f1-117">Requirements</span></span>



| <span data-ttu-id="e11f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11f1-118">Requirement</span></span> | <span data-ttu-id="e11f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e11f1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e11f1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e11f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e11f1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e11f1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e11f1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e11f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e11f1-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e11f1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e11f1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e11f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e11f1-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e11f1-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11f1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e11f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11f1-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e11f1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e11f1-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e11f1-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e11f1-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="e11f1-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




