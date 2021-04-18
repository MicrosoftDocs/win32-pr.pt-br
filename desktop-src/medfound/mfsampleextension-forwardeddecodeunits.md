---
description: Obtém um objeto do tipo IMFCollection que contém objetos IMFSample que contêm NALUs (unidades de camada de abstração de rede) e unidades SEI (informações de aprimoramento complementar) encaminhadas por um decodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Atributo MFSampleExtension_ForwardedDecodeUnits (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765151"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="09ae5-103">\_Atributo MFSampleExtension ForwardedDecodeUnits</span><span class="sxs-lookup"><span data-stu-id="09ae5-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="09ae5-104">Obtém um objeto do tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contém objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contêm NALUs (unidades de camada de abstração de rede) e unidades sei (informações de aprimoramento complementar) encaminhadas por um decodificador.</span><span class="sxs-lookup"><span data-stu-id="09ae5-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="09ae5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="09ae5-105">Data type</span></span>

<span data-ttu-id="09ae5-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="09ae5-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="09ae5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="09ae5-107">Remarks</span></span>

<span data-ttu-id="09ae5-108">A coleção contém todas as unidades NALU/SEI personalizadas desde o quadro anterior com bytes de prevenção de emulação removidos.</span><span class="sxs-lookup"><span data-stu-id="09ae5-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ae5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09ae5-109">Requirements</span></span>



| <span data-ttu-id="09ae5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ae5-110">Requirement</span></span> | <span data-ttu-id="09ae5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="09ae5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09ae5-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09ae5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="09ae5-113">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="09ae5-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09ae5-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09ae5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="09ae5-115">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="09ae5-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09ae5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09ae5-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ae5-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ae5-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




