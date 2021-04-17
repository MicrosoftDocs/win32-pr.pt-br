---
description: Um valor que indica o tipo de sensor fornecido por uma fonte de quadro, como cor, infravermelho ou profundidade.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Atributo MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754860"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="e3f7b-103">\_Atributo de \_ tipos de framery MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e3f7b-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="e3f7b-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e3f7b-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e3f7b-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e3f7b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e3f7b-106">Um valor que indica o tipo de sensor fornecido por uma fonte de quadro, como cor, infravermelho ou profundidade.</span><span class="sxs-lookup"><span data-stu-id="e3f7b-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3f7b-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e3f7b-107">Data type</span></span>

<span data-ttu-id="e3f7b-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3f7b-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f7b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3f7b-109">Remarks</span></span>

<span data-ttu-id="e3f7b-110">Esse valor deve ser um membro da enumeração [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e3f7b-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="e3f7b-111">Para compatibilidade com versões anteriores, quando esse atributo não está definido em um tipo de mídia, supõe-se que **\_ MFFrameSourceTyes:: Color**.</span><span class="sxs-lookup"><span data-stu-id="e3f7b-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f7b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f7b-112">Requirements</span></span>



| <span data-ttu-id="e3f7b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f7b-113">Requirement</span></span> | <span data-ttu-id="e3f7b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e3f7b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f7b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3f7b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f7b-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e3f7b-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e3f7b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3f7b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f7b-118">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e3f7b-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="e3f7b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3f7b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f7b-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f7b-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
