---
description: Especifica se o modo alfa para tipos de vídeo de mídia de cor é premultiplicado ou reto.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Atributo MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011099"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="3b123-103">\_Atributo de \_ \_ modo alfa do MF MT</span><span class="sxs-lookup"><span data-stu-id="3b123-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="3b123-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3b123-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b123-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3b123-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b123-106">Especifica se o modo alfa para tipos de vídeo de mídia de cor é premultiplicado ou reto.</span><span class="sxs-lookup"><span data-stu-id="3b123-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="3b123-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3b123-107">Data type</span></span>

<span data-ttu-id="3b123-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3b123-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b123-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b123-109">Remarks</span></span>

<span data-ttu-id="3b123-110">Esse valor pode ser convertido em um valor de [**\_ \_ modo alfa dxgi**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) .</span><span class="sxs-lookup"><span data-stu-id="3b123-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="3b123-111">Se esse atributo não estiver presente, para compatibilidade com versões anteriores, o valor será o **\_ modo alfa de dxgi \_ \_ direto** para formato de vídeo com suporte para o canal alfa, como ARGB32 ou o **\_ modo alfa de dxgi \_ \_ ignorar** para formato de vídeo sem canal alfa, como RGB32.</span><span class="sxs-lookup"><span data-stu-id="3b123-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b123-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b123-112">Requirements</span></span>



| <span data-ttu-id="3b123-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b123-113">Requirement</span></span> | <span data-ttu-id="3b123-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3b123-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b123-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b123-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b123-116">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3b123-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b123-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b123-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b123-118">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3b123-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="3b123-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b123-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b123-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b123-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
