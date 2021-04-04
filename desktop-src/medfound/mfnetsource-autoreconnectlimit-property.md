---
description: O número de vezes que a origem da rede tenta se reconectar ao servidor e retomar o streaming se a conexão for perdida.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: Propriedade MFNETSOURCE_AUTORECONNECTLIMIT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647558"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="d3fe7-103">\_Propriedade MFNETSOURCE AUTORECONNECTLIMIT</span><span class="sxs-lookup"><span data-stu-id="d3fe7-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="d3fe7-104">O número de vezes que a origem da rede tenta se reconectar ao servidor e retomar o streaming se a conexão for perdida.</span><span class="sxs-lookup"><span data-stu-id="d3fe7-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="d3fe7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d3fe7-105">Data type</span></span>

<span data-ttu-id="d3fe7-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d3fe7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d3fe7-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d3fe7-107">PROPVARIANT member</span></span>

<span data-ttu-id="d3fe7-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="d3fe7-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="d3fe7-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d3fe7-109">VT\_I4</span></span>

<span data-ttu-id="d3fe7-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d3fe7-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d3fe7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3fe7-111">Remarks</span></span>

<span data-ttu-id="d3fe7-112">A constante **MFNETSOURCE \_ AUTORECONNECTLIMIT** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d3fe7-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="d3fe7-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="d3fe7-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d3fe7-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="d3fe7-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d3fe7-115">Para definir a propriedade, passe um objeto **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d3fe7-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="d3fe7-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d3fe7-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3fe7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3fe7-117">Requirements</span></span>



| <span data-ttu-id="d3fe7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3fe7-118">Requirement</span></span> | <span data-ttu-id="d3fe7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d3fe7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3fe7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3fe7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3fe7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d3fe7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3fe7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3fe7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3fe7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3fe7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3fe7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3fe7-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3fe7-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3fe7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3fe7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe7-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3fe7-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d3fe7-128">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="d3fe7-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="d3fe7-129">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3fe7-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




