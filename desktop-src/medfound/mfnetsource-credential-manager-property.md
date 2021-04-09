---
description: Contém um ponteiro para a interface IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Propriedade MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090854"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="1c9fa-103">Propriedade do Gerenciador de \_ credenciais MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="1c9fa-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="1c9fa-104">Contém um ponteiro para a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="1c9fa-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="1c9fa-105">Use essa propriedade para passar a implementação do aplicativo de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) para a fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="1c9fa-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="1c9fa-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1c9fa-106">Data type</span></span>

<span data-ttu-id="1c9fa-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1c9fa-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1c9fa-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1c9fa-108">PROPVARIANT member</span></span>

<span data-ttu-id="1c9fa-109">Ponteiro **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="1c9fa-109">**IUnknown** pointer</span></span>

<span data-ttu-id="1c9fa-110">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="1c9fa-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="1c9fa-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="1c9fa-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1c9fa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c9fa-112">Remarks</span></span>

<span data-ttu-id="1c9fa-113">A constante **MFNETSOURCE \_ Credential \_ Manager** define o **GUID** para a chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1c9fa-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="1c9fa-114">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="1c9fa-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9fa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c9fa-115">Requirements</span></span>



| <span data-ttu-id="1c9fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c9fa-116">Requirement</span></span> | <span data-ttu-id="1c9fa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1c9fa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9fa-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c9fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9fa-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c9fa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c9fa-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c9fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9fa-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c9fa-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c9fa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c9fa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c9fa-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c9fa-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c9fa-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c9fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9fa-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c9fa-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1c9fa-126">Autenticação de origem da rede</span><span class="sxs-lookup"><span data-stu-id="1c9fa-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="1c9fa-127">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c9fa-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




