---
description: O número de vezes que a fonte de rede tentou reconectar-se à rede.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: Propriedade MFNETSOURCE_AUTORECONNECTPROGRESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785922"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="9c15b-103">\_Propriedade MFNETSOURCE AUTORECONNECTPROGRESS</span><span class="sxs-lookup"><span data-stu-id="9c15b-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="9c15b-104">O número de vezes que a fonte de rede tentou reconectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="9c15b-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="9c15b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9c15b-105">Data type</span></span>

<span data-ttu-id="9c15b-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9c15b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9c15b-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9c15b-107">PROPVARIANT member</span></span>

<span data-ttu-id="9c15b-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="9c15b-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="9c15b-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="9c15b-109">VT\_I4</span></span>

<span data-ttu-id="9c15b-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="9c15b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="9c15b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c15b-111">Remarks</span></span>

<span data-ttu-id="9c15b-112">A constante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9c15b-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="9c15b-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="9c15b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="9c15b-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9c15b-114">This property is read-only.</span></span> <span data-ttu-id="9c15b-115">Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="9c15b-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c15b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c15b-116">Requirements</span></span>



| <span data-ttu-id="9c15b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c15b-117">Requirement</span></span> | <span data-ttu-id="9c15b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9c15b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c15b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c15b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c15b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c15b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c15b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c15b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c15b-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c15b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c15b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c15b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c15b-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c15b-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c15b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c15b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c15b-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c15b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9c15b-127">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="9c15b-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="9c15b-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c15b-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




