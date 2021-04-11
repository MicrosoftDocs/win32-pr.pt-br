---
description: Identificador exclusivo pelo qual o servidor identifica o cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Propriedade MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090855"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="f94fc-103">\_Propriedade MFNETSOURCE CLIENTGUID</span><span class="sxs-lookup"><span data-stu-id="f94fc-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="f94fc-104">Identificador exclusivo pelo qual o servidor identifica o cliente.</span><span class="sxs-lookup"><span data-stu-id="f94fc-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="f94fc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f94fc-105">Data type</span></span>

<span data-ttu-id="f94fc-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f94fc-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f94fc-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f94fc-107">PROPVARIANT member</span></span>

<span data-ttu-id="f94fc-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f94fc-108">**GUID**</span></span>

<span data-ttu-id="f94fc-109">CLSID do VT \_</span><span class="sxs-lookup"><span data-stu-id="f94fc-109">VT\_CLSID</span></span>

<span data-ttu-id="f94fc-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="f94fc-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="f94fc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f94fc-111">Remarks</span></span>

<span data-ttu-id="f94fc-112">A constante **MFNETSOURCE \_ CLIENTGUID** define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f94fc-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="f94fc-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="f94fc-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="f94fc-114">Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="f94fc-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f94fc-115">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f94fc-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="f94fc-116">Se não for definido ou definido como **GUID \_ NULL**, Microsoft Media Foundation gerará um GUID anônimo por sessão que garanta a privacidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="f94fc-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94fc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f94fc-117">Requirements</span></span>



| <span data-ttu-id="f94fc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f94fc-118">Requirement</span></span> | <span data-ttu-id="f94fc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f94fc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f94fc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f94fc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f94fc-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f94fc-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f94fc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f94fc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f94fc-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f94fc-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f94fc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f94fc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f94fc-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94fc-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f94fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94fc-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f94fc-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f94fc-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f94fc-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




