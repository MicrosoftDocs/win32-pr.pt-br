---
description: Representa o tipo de origem do quadro.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Atributo MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763280"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="2c6f7-103">\_Atributo de \_ \_ tipos de framery de atributo MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="2c6f7-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="2c6f7-104">Representa o tipo de origem do quadro.</span><span class="sxs-lookup"><span data-stu-id="2c6f7-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c6f7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2c6f7-105">Data type</span></span>

<span data-ttu-id="2c6f7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2c6f7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c6f7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c6f7-107">Remarks</span></span>

<span data-ttu-id="2c6f7-108">Esse valor desse atributo deve ser um bitmask de um ou mais valores da enumeração [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) .</span><span class="sxs-lookup"><span data-stu-id="2c6f7-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="2c6f7-109">Para dar suporte à compatibilidade com versões anteriores, quando esse atributo não está definido para um tipo de mídia, supõe-se que o valor é **MFFrameSourceTypes:: Color**.</span><span class="sxs-lookup"><span data-stu-id="2c6f7-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6f7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c6f7-110">Requirements</span></span>



| <span data-ttu-id="2c6f7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c6f7-111">Requirement</span></span> | <span data-ttu-id="2c6f7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2c6f7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6f7-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c6f7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6f7-114">\[Somente aplicativos da área de trabalho do Windows 10, versão 1607\]</span><span class="sxs-lookup"><span data-stu-id="2c6f7-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2c6f7-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c6f7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6f7-116">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2c6f7-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2c6f7-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c6f7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6f7-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c6f7-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




