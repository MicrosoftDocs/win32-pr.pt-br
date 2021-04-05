---
description: Duração do streaming acelerado para a fonte de rede, em milissegundos.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Propriedade MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827413"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="c5145-103">\_Propriedade MFNETSOURCE ACCELERATEDSTREAMINGDURATION</span><span class="sxs-lookup"><span data-stu-id="c5145-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="c5145-104">Duração do streaming acelerado para a fonte de rede, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c5145-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="c5145-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c5145-105">Data type</span></span>

<span data-ttu-id="c5145-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c5145-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c5145-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c5145-107">PROPVARIANT member</span></span>

<span data-ttu-id="c5145-108">**DWORD** (armazenado como **longo**)</span><span class="sxs-lookup"><span data-stu-id="c5145-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="c5145-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="c5145-109">VT\_I4</span></span>

<span data-ttu-id="c5145-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="c5145-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c5145-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5145-111">Remarks</span></span>

<span data-ttu-id="c5145-112">A constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c5145-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="c5145-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="c5145-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c5145-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="c5145-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c5145-115">Para definir a propriedade, passe um objeto **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="c5145-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="c5145-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c5145-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="c5145-117">Essa propriedade se aplica ao recurso de início rápido do Windows Media Services, que reproduz conteúdo rapidamente sem aguardar o buffer inicial longo.</span><span class="sxs-lookup"><span data-stu-id="c5145-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="c5145-118">Ao usar o início rápido, o servidor que executa o Windows Media Services enviará alguns dados no início do conteúdo a uma taxa mais rápida do que a especificada pela taxa de bits do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c5145-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="c5145-119">O valor padrão dessa propriedade é 10.000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c5145-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5145-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5145-120">Requirements</span></span>



| <span data-ttu-id="c5145-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5145-121">Requirement</span></span> | <span data-ttu-id="c5145-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c5145-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5145-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5145-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c5145-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5145-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5145-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5145-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c5145-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5145-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5145-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5145-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5145-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5145-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5145-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5145-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5145-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5145-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c5145-131">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="c5145-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="c5145-132">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5145-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




