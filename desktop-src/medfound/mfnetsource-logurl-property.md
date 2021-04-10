---
description: Lista de URLs para as quais a fonte de rede enviará informações de log.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Propriedade MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090687"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="bd5b9-103">\_Propriedade MFNETSOURCE LogURL</span><span class="sxs-lookup"><span data-stu-id="bd5b9-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="bd5b9-104">Lista de URLs para as quais a fonte de rede enviará informações de log.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="bd5b9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bd5b9-105">Data type</span></span>

<span data-ttu-id="bd5b9-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="bd5b9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bd5b9-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="bd5b9-107">PROPVARIANT member</span></span>

<span data-ttu-id="bd5b9-108">Matriz de cadeias de caracteres largos (**CALPWSTR**)</span><span class="sxs-lookup"><span data-stu-id="bd5b9-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="bd5b9-109">\_LPWStr do vetor VT VT \| \_</span><span class="sxs-lookup"><span data-stu-id="bd5b9-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="bd5b9-110">**calpwstr**</span><span class="sxs-lookup"><span data-stu-id="bd5b9-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="bd5b9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd5b9-111">Remarks</span></span>

<span data-ttu-id="bd5b9-112">A constante **MFNETSOURCE \_ LogURL** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="bd5b9-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bd5b9-114">Os aplicativos podem usar essa propriedade para configurar a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="bd5b9-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bd5b9-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5b9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd5b9-117">Requirements</span></span>



| <span data-ttu-id="bd5b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd5b9-118">Requirement</span></span> | <span data-ttu-id="bd5b9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bd5b9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5b9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd5b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5b9-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd5b9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd5b9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd5b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5b9-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd5b9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd5b9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd5b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5b9-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd5b9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5b9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd5b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5b9-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd5b9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bd5b9-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd5b9-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




