---
description: Especifica a definição de configuração para o localizador de proxy padrão.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Propriedade MFNETSOURCE_PROXYSETTINGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091151"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="92d9a-103">\_Propriedade MFNETSOURCE PROXYSETTINGS</span><span class="sxs-lookup"><span data-stu-id="92d9a-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="92d9a-104">Especifica a definição de configuração para o localizador de proxy padrão.</span><span class="sxs-lookup"><span data-stu-id="92d9a-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="92d9a-105">O valor dessa propriedade é um membro da enumeração [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .</span><span class="sxs-lookup"><span data-stu-id="92d9a-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="92d9a-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="92d9a-106">Data type</span></span>

<span data-ttu-id="92d9a-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="92d9a-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="92d9a-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="92d9a-108">PROPVARIANT member</span></span>

<span data-ttu-id="92d9a-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="92d9a-109">**LONG**</span></span>

<span data-ttu-id="92d9a-110">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="92d9a-110">VT\_I4</span></span>

<span data-ttu-id="92d9a-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="92d9a-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="92d9a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92d9a-112">Remarks</span></span>

<span data-ttu-id="92d9a-113">A constante **MFNETSOURCE \_ PROXYSETTINGS** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="92d9a-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="92d9a-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="92d9a-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="92d9a-115">Os aplicativos podem usar essa propriedade para configurar o localizador de proxy ao criar o objeto de localizador de proxy padrão.</span><span class="sxs-lookup"><span data-stu-id="92d9a-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="92d9a-116">Para definir a propriedade, passe um ponteiro **IPropertyStore** no parâmetro *PProxyConfig* da função [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="92d9a-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="92d9a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d9a-117">Requirements</span></span>



| <span data-ttu-id="92d9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d9a-118">Requirement</span></span> | <span data-ttu-id="92d9a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="92d9a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92d9a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92d9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92d9a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92d9a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92d9a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92d9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92d9a-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92d9a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92d9a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92d9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92d9a-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92d9a-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92d9a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="92d9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d9a-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92d9a-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="92d9a-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92d9a-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="92d9a-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="92d9a-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




