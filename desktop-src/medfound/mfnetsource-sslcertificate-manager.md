---
description: Armazena o ponteiro IUnknown da classe que implementa a interface IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: Propriedade MFNETSOURCE_SSLCERTIFICATE_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787699"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="aeb12-103">\_Propriedade MFNETSOURCE SSLCERTIFICATE \_ Manager</span><span class="sxs-lookup"><span data-stu-id="aeb12-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="aeb12-104">Armazena o ponteiro **IUnknown** da classe que implementa a interface [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) .</span><span class="sxs-lookup"><span data-stu-id="aeb12-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="aeb12-105">A implementação do cliente fornece métodos para obter o certificado SSL do cliente quando ele é solicitado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="aeb12-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="aeb12-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aeb12-106">Data type</span></span>

<span data-ttu-id="aeb12-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="aeb12-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="aeb12-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="aeb12-108">PROPVARIANT member</span></span>

<span data-ttu-id="aeb12-109">**Ponteiro IUnknown**</span><span class="sxs-lookup"><span data-stu-id="aeb12-109">**IUnknown pointer**</span></span>

<span data-ttu-id="aeb12-110">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="aeb12-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="aeb12-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="aeb12-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="aeb12-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeb12-112">Remarks</span></span>

<span data-ttu-id="aeb12-113">A constante **MFNETSOURCE \_ SSLCERTIFICATE \_ Manager** define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="aeb12-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="aeb12-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="aeb12-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="aeb12-115">Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="aeb12-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="aeb12-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="aeb12-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb12-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb12-117">Requirements</span></span>



| <span data-ttu-id="aeb12-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb12-118">Requirement</span></span> | <span data-ttu-id="aeb12-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb12-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb12-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb12-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aeb12-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aeb12-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb12-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="aeb12-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="aeb12-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aeb12-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb12-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb12-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb12-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeb12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb12-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aeb12-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aeb12-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aeb12-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




