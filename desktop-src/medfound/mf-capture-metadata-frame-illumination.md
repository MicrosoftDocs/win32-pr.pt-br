---
description: Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Atributo MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763929"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="6f06d-103">\_Atributo de \_ iluminação de quadro de metadados de captura MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f06d-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="6f06d-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="6f06d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f06d-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="6f06d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6f06d-106">Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).</span><span class="sxs-lookup"><span data-stu-id="6f06d-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f06d-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6f06d-107">Data type</span></span>

<span data-ttu-id="6f06d-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="6f06d-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f06d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f06d-109">Remarks</span></span>

<span data-ttu-id="6f06d-110">Esse atributo é um bitmask.</span><span class="sxs-lookup"><span data-stu-id="6f06d-110">This attribute is a bitmask.</span></span> <span data-ttu-id="6f06d-111">É um valor de 64 bits para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6f06d-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="6f06d-112">A iluminação ativa é quando um dispositivo tem um emissor de luz próximo à câmera IR emitindo um feixe de luz para iluminar a cena, normalmente emitindo luz de IR para que não incomodar os olhos humanos.</span><span class="sxs-lookup"><span data-stu-id="6f06d-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="6f06d-113">Defina valor como (valor & 0x1)! = 0 se o quadro foi capturado quando a iluminação ativa estava ativada e definida (valor & 0x1) = = 0 se a iluminação ativa estava desligada.</span><span class="sxs-lookup"><span data-stu-id="6f06d-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f06d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f06d-114">Requirements</span></span>



| <span data-ttu-id="6f06d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f06d-115">Requirement</span></span> | <span data-ttu-id="6f06d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6f06d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f06d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f06d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f06d-118">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="6f06d-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6f06d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f06d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f06d-120">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="6f06d-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="6f06d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f06d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f06d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f06d-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




