---
description: Fornece uma instância de IMFMuxStreamAttributesManager que gerencia o IMFAttributes que descreve os subfluxos de uma fonte de mídia multiplexada.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Atributo MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748878"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="707b1-103">\_Atributo de \_ Gerenciador de multiplexado de DEVICESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="707b1-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="707b1-104">Fornece uma instância de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) que gerencia o [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) que descreve os subfluxos de uma fonte de mídia multiplexada.</span><span class="sxs-lookup"><span data-stu-id="707b1-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="707b1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="707b1-105">Data type</span></span>

<span data-ttu-id="707b1-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="707b1-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="707b1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="707b1-107">Remarks</span></span>

<span data-ttu-id="707b1-108">Passe esse valor em [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para determinar se a origem da mídia fornece fluxos multiplexados e, nesse caso, obter uma instância de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span><span class="sxs-lookup"><span data-stu-id="707b1-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="707b1-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="707b1-109">Requirements</span></span>



| <span data-ttu-id="707b1-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="707b1-110">Requirement</span></span> | <span data-ttu-id="707b1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="707b1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="707b1-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707b1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="707b1-113">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="707b1-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="707b1-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707b1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="707b1-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="707b1-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="707b1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="707b1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="707b1-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
