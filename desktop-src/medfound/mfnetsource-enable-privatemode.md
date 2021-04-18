---
description: Habilita o modo de download particular na fonte de rede.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Propriedade MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790384"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="c98b5-103">MFNETSOURCE \_ habilitar \_ Propriedade particularmode</span><span class="sxs-lookup"><span data-stu-id="c98b5-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="c98b5-104">Habilita o modo de download particular na fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="c98b5-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="c98b5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c98b5-105">Data type</span></span>

<span data-ttu-id="c98b5-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c98b5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c98b5-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c98b5-107">PROPVARIANT member</span></span>

<span data-ttu-id="c98b5-108">**BOOL**</span><span class="sxs-lookup"><span data-stu-id="c98b5-108">**BOOL**</span></span>

<span data-ttu-id="c98b5-109">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="c98b5-109">VT\_I4</span></span>

<span data-ttu-id="c98b5-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="c98b5-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c98b5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c98b5-111">Remarks</span></span>

<span data-ttu-id="c98b5-112">Se essa propriedade for **true**, o cache será limpo quando a sessão terminar.</span><span class="sxs-lookup"><span data-stu-id="c98b5-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="c98b5-113">A constante **MFNETSOURCE \_ CLIENTGUID** define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c98b5-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="c98b5-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="c98b5-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="c98b5-115">Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="c98b5-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c98b5-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c98b5-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c98b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c98b5-117">Requirements</span></span>



| <span data-ttu-id="c98b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c98b5-118">Requirement</span></span> | <span data-ttu-id="c98b5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c98b5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c98b5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c98b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c98b5-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c98b5-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c98b5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c98b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c98b5-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c98b5-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c98b5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c98b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c98b5-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c98b5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c98b5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c98b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98b5-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c98b5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c98b5-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c98b5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




