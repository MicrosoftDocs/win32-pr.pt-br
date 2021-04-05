---
description: Armazena uma matriz de bytes que representa a licença DRM associada ao fluxo de bytes.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Propriedade MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647556"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="59c71-103">\_Propriedade de \_ representação de licença MFNETSOURCE DRMNET \_</span><span class="sxs-lookup"><span data-stu-id="59c71-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="59c71-104">Armazena uma matriz de bytes que representa a licença DRM associada ao fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="59c71-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="59c71-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="59c71-105">Data type</span></span>

<span data-ttu-id="59c71-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="59c71-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="59c71-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="59c71-107">PROPVARIANT member</span></span>

<span data-ttu-id="59c71-108">Matriz de bytes (**blob**)</span><span class="sxs-lookup"><span data-stu-id="59c71-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="59c71-109">\_blob VT</span><span class="sxs-lookup"><span data-stu-id="59c71-109">VT\_BLOB</span></span>

<span data-ttu-id="59c71-110">**blob**</span><span class="sxs-lookup"><span data-stu-id="59c71-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="59c71-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="59c71-111">Remarks</span></span>

<span data-ttu-id="59c71-112">A **representação de \_ \_ licença DRMNET \_ constante MFNETSOURCE** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="59c71-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="59c71-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="59c71-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="59c71-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="59c71-114">This property is read-only.</span></span> <span data-ttu-id="59c71-115">Para obter o valor da Propriedade do fluxo de bytes de rede, chame **IPropertyStore:: GetValue** e passe a estrutura **PROPERTYKEY** no parâmetro de *chave* .</span><span class="sxs-lookup"><span data-stu-id="59c71-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="59c71-116">O membro **fmtid** de **PROPERTYKEY** deve ser definido como a propriedade GUID.</span><span class="sxs-lookup"><span data-stu-id="59c71-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c71-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c71-117">Requirements</span></span>



| <span data-ttu-id="59c71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c71-118">Requirement</span></span> | <span data-ttu-id="59c71-119">Valor</span><span class="sxs-lookup"><span data-stu-id="59c71-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59c71-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59c71-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59c71-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59c71-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59c71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59c71-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59c71-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59c71-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59c71-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c71-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c71-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c71-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="59c71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c71-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59c71-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="59c71-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59c71-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




