---
description: Armazena o nome do host e a porta do servidor proxy usado pela fonte de rede.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: Propriedade MFNETSOURCE_PROXYINFO (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780389"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="6a2eb-103">\_Propriedade MFNETSOURCE PROXYINFO</span><span class="sxs-lookup"><span data-stu-id="6a2eb-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="6a2eb-104">Armazena o nome do host e a porta do servidor proxy usado pela fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="6a2eb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6a2eb-105">Data type</span></span>

<span data-ttu-id="6a2eb-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6a2eb-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6a2eb-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6a2eb-107">PROPVARIANT member</span></span>

<span data-ttu-id="6a2eb-108">Cadeia de caracteres largos (**WCHAR** \* )</span><span class="sxs-lookup"><span data-stu-id="6a2eb-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="6a2eb-109">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="6a2eb-109">VT\_LPWSTR</span></span>

<span data-ttu-id="6a2eb-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="6a2eb-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6a2eb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a2eb-111">Remarks</span></span>

<span data-ttu-id="6a2eb-112">A constante **MFNETSOURCE \_ PROXYINFO** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="6a2eb-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6a2eb-114">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-114">This property is read-only.</span></span> <span data-ttu-id="6a2eb-115">Para obter o valor da propriedade da origem da rede, chame **IPropertyStore:: GetValue** e passe a estrutura **PROPERTYKEY** no parâmetro *Key* .</span><span class="sxs-lookup"><span data-stu-id="6a2eb-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="6a2eb-116">O membro **fmtid** de **PROPERTYKEY** deve ser definido como a propriedade GUID.</span><span class="sxs-lookup"><span data-stu-id="6a2eb-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a2eb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a2eb-117">Requirements</span></span>



| <span data-ttu-id="6a2eb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a2eb-118">Requirement</span></span> | <span data-ttu-id="6a2eb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6a2eb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2eb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a2eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a2eb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a2eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a2eb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a2eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a2eb-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a2eb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a2eb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a2eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a2eb-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a2eb-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a2eb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a2eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2eb-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a2eb-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6a2eb-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a2eb-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6a2eb-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="6a2eb-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




