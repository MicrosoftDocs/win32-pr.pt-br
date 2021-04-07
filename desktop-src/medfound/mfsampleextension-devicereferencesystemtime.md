---
description: Especifica o carimbo de data/hora do dispositivo original no exemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Atributo MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827543"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="21576-103">\_Atributo MFSampleExtension DeviceReferenceSystemTime</span><span class="sxs-lookup"><span data-stu-id="21576-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="21576-104">Especifica o carimbo de data/hora do dispositivo original no exemplo.</span><span class="sxs-lookup"><span data-stu-id="21576-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="21576-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="21576-105">Data type</span></span>

<span data-ttu-id="21576-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="21576-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="21576-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="21576-107">Remarks</span></span>

<span data-ttu-id="21576-108">Este é um carimbo de data/hora de referência de dispositivo de amostras de mídia em resolução de 100ns.</span><span class="sxs-lookup"><span data-stu-id="21576-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="21576-109">Esse carimbo de data/hora pode ou não transportar o valor real do contador de desempenho de consulta (QPC), dependendo da origem que produz os exemplos.</span><span class="sxs-lookup"><span data-stu-id="21576-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="21576-110">Esse valor pode ser modificado por outros componentes no pipeline de mídia.</span><span class="sxs-lookup"><span data-stu-id="21576-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="21576-111">Esse valor não está disponível para MFTs inserido no pipeline de captura.</span><span class="sxs-lookup"><span data-stu-id="21576-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="21576-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21576-112">Requirements</span></span>



| <span data-ttu-id="21576-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="21576-113">Requirement</span></span> | <span data-ttu-id="21576-114">Valor</span><span class="sxs-lookup"><span data-stu-id="21576-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21576-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21576-115">Minimum supported client</span></span><br/> | <span data-ttu-id="21576-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21576-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="21576-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21576-117">Minimum supported server</span></span><br/> | <span data-ttu-id="21576-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="21576-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21576-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21576-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="21576-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="21576-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="21576-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="21576-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21576-122"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21576-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21576-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="21576-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21576-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21576-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




