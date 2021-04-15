---
description: Especifica que os tipos de unidade da camada de abstração de rede (NAL) devem ser encaminhados nos exemplos de saída pelo decodificador.
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: Atributo MF_MT_FORWARD_CUSTOM_NALU (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506159"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="1fb65-103">\_ \_ \_ Atributo NALU personalizado de encaminhamento MF MT \_</span><span class="sxs-lookup"><span data-stu-id="1fb65-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="1fb65-104">Especifica que os tipos de unidade da camada de abstração de rede (NAL) devem ser encaminhados nos exemplos de saída pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="1fb65-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="1fb65-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1fb65-105">Data type</span></span>

<span data-ttu-id="1fb65-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1fb65-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb65-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fb65-107">Remarks</span></span>

<span data-ttu-id="1fb65-108">Se o decodificador analisar um NALU, ele não será encaminhado.</span><span class="sxs-lookup"><span data-stu-id="1fb65-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb65-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb65-109">Requirements</span></span>



| <span data-ttu-id="1fb65-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb65-110">Requirement</span></span> | <span data-ttu-id="1fb65-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb65-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb65-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fb65-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb65-113">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="1fb65-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1fb65-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fb65-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb65-115">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1fb65-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1fb65-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fb65-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb65-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb65-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




