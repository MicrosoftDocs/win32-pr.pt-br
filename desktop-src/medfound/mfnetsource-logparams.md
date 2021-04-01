---
description: Matriz de cadeias de caracteres com os parâmetros a serem enviados ao servidor de log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Propriedade MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921265"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="d5e68-103">\_Propriedade MFNETSOURCE LOGPARAMS</span><span class="sxs-lookup"><span data-stu-id="d5e68-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="d5e68-104">Matriz de cadeias de caracteres com os parâmetros a serem enviados ao servidor de log.</span><span class="sxs-lookup"><span data-stu-id="d5e68-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="d5e68-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5e68-105">Data type</span></span>

<span data-ttu-id="d5e68-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d5e68-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d5e68-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d5e68-107">PROPVARIANT member</span></span>

<span data-ttu-id="d5e68-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d5e68-108">\**WCHAR\** _</span></span>

<span data-ttu-id="d5e68-109">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="d5e68-109">VT\_LPWSTR</span></span>

<span data-ttu-id="d5e68-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="d5e68-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="d5e68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5e68-111">Remarks</span></span>

<span data-ttu-id="d5e68-112">A constante **MFNETSOURCE \_ LOGPARAMS** define o GUID da chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d5e68-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="d5e68-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="d5e68-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="d5e68-114">Para definir essa propriedade na fonte de rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d5e68-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d5e68-115">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d5e68-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e68-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e68-116">Requirements</span></span>



| <span data-ttu-id="d5e68-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e68-117">Requirement</span></span> | <span data-ttu-id="d5e68-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d5e68-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e68-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5e68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e68-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d5e68-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5e68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e68-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d5e68-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d5e68-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5e68-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e68-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e68-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e68-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5e68-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e68-126">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5e68-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d5e68-127">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5e68-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




