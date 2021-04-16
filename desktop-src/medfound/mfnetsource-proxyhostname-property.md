---
description: Especifica o nome do host do servidor proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: Propriedade MFNETSOURCE_PROXYHOSTNAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768309"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="4eb95-103">\_Propriedade MFNETSOURCE PROXYHOSTNAME</span><span class="sxs-lookup"><span data-stu-id="4eb95-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="4eb95-104">Especifica o nome do host do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="4eb95-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="4eb95-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4eb95-105">Data type</span></span>

<span data-ttu-id="4eb95-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="4eb95-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4eb95-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4eb95-107">PROPVARIANT member</span></span>

<span data-ttu-id="4eb95-108">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="4eb95-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="4eb95-109">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="4eb95-109">VT\_LPWSTR</span></span>

<span data-ttu-id="4eb95-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="4eb95-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4eb95-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4eb95-111">Remarks</span></span>

<span data-ttu-id="4eb95-112">A constante **MFNETSOURCE \_ PROXYHOSTNAME** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="4eb95-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="4eb95-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="4eb95-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4eb95-114">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy padrão ao criar o objeto de localizador de proxy.</span><span class="sxs-lookup"><span data-stu-id="4eb95-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="4eb95-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="4eb95-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="4eb95-116">Essa propriedade deve ser definida pelo aplicativo quando o localizador de proxy estiver configurado para operar no modo manual.</span><span class="sxs-lookup"><span data-stu-id="4eb95-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb95-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eb95-117">Requirements</span></span>



| <span data-ttu-id="4eb95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb95-118">Requirement</span></span> | <span data-ttu-id="4eb95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4eb95-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb95-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4eb95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb95-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4eb95-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4eb95-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4eb95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb95-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4eb95-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4eb95-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4eb95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb95-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb95-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb95-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4eb95-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb95-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eb95-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4eb95-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4eb95-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="4eb95-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="4eb95-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




