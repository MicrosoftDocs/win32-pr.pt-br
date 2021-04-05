---
description: Contém o código de erro da falha de conexão mais recente para este nó topologia.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Atributo MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090868"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="e5c8d-103">\_Atributo MF TOPONODE \_ ERRORCODE</span><span class="sxs-lookup"><span data-stu-id="e5c8d-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="e5c8d-104">Contém o código de erro da falha de conexão mais recente para este nó topologia.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e5c8d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e5c8d-105">Data type</span></span>

<span data-ttu-id="e5c8d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5c8d-106">**UINT32**</span></span>

<span data-ttu-id="e5c8d-107">Ttreat como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5c8d-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c8d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5c8d-108">Remarks</span></span>

<span data-ttu-id="e5c8d-109">Esse atributo se aplica a todos os tipos de nó.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="e5c8d-110">O valor desse atributo é um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5c8d-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="e5c8d-111">A sessão de mídia ou o carregador de topologia pode definir o atributo.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="e5c8d-112">Normalmente, os aplicativos lêem esse atributo, mas não os definem.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="e5c8d-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e5c8d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c8d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5c8d-114">Requirements</span></span>



| <span data-ttu-id="e5c8d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c8d-115">Requirement</span></span> | <span data-ttu-id="e5c8d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c8d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c8d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5c8d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c8d-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5c8d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5c8d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5c8d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c8d-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5c8d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e5c8d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5c8d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c8d-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c8d-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c8d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5c8d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c8d-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5c8d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e5c8d-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e5c8d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e5c8d-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e5c8d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e5c8d-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e5c8d-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e5c8d-128">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="e5c8d-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




