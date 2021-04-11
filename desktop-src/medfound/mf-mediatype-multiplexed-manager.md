---
description: Fornece uma instância de IMFMuxStreamMediaTypeManager que pode ser usada para obter os tipos de mídia dos subfluxos de uma fonte de mídia multiplexada, bem como controlar a combinação de subfluxos que são multiplexados pela origem.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Atributo MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172472"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a><span data-ttu-id="46932-103">\_Atributo do \_ Gerenciador de MediaType do MF \_</span><span class="sxs-lookup"><span data-stu-id="46932-103">MF\_MEDIATYPE\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="46932-104">Fornece uma instância de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) que pode ser usada para obter os tipos de mídia dos subfluxos de uma fonte de mídia multiplexada, bem como controlar a combinação de subfluxos que são multiplexados pela origem.</span><span class="sxs-lookup"><span data-stu-id="46932-104">Provides an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) which can be used to get the media types of the substreams of a multiplexed media source as well as control the combination of substreams that are multiplexed by the source.</span></span>

## <a name="data-type"></a><span data-ttu-id="46932-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="46932-105">Data type</span></span>

<span data-ttu-id="46932-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="46932-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="46932-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="46932-107">Remarks</span></span>

<span data-ttu-id="46932-108">Passe esse valor em [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obter uma instância de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span><span class="sxs-lookup"><span data-stu-id="46932-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="46932-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46932-109">Requirements</span></span>



| <span data-ttu-id="46932-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="46932-110">Requirement</span></span> | <span data-ttu-id="46932-111">Valor</span><span class="sxs-lookup"><span data-stu-id="46932-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46932-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46932-112">Minimum supported client</span></span><br/> | <span data-ttu-id="46932-113">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="46932-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="46932-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46932-114">Minimum supported server</span></span><br/> | <span data-ttu-id="46932-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="46932-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="46932-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46932-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="46932-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46932-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
