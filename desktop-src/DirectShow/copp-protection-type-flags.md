---
description: As constantes a seguir são usadas com o protocolo COPP (certificado de proteção de saída) para mecanismos de proteção de saída específicos.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Sinalizadores de tipo de proteção COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787397"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="40257-103">Sinalizadores de tipo de proteção COPP</span><span class="sxs-lookup"><span data-stu-id="40257-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="40257-104">As constantes a seguir são usadas com o protocolo COPP (certificado de proteção de saída) para mecanismos de proteção de saída específicos.</span><span class="sxs-lookup"><span data-stu-id="40257-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="40257-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="40257-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="40257-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="40257-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="40257-107"><dt>**Copp \_ ProtectionType \_ desconhecido**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="40257-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="40257-108">Mecanismo de proteção desconhecido.</span><span class="sxs-lookup"><span data-stu-id="40257-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="40257-109"><dt>**Copp \_ ProtectionType \_ nenhum**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="40257-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="40257-110">Nenhum mecanismo de proteção.</span><span class="sxs-lookup"><span data-stu-id="40257-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="40257-111"><dt>**Copp \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="40257-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="40257-112">High-Bandwidth Proteção de Conteúdo Digital (HDCP).</span><span class="sxs-lookup"><span data-stu-id="40257-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="40257-113"><dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="40257-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="40257-114">Proteção de cópia analógica (ACP).</span><span class="sxs-lookup"><span data-stu-id="40257-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="40257-115"><dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="40257-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="40257-116">Sistema de gerenciamento de geração de cópia analógico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="40257-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="40257-117"><dt>**Copp \_ ProtectionType \_ máscara**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="40257-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="40257-118">Bitmask para isolar sinalizadores válidos.</span><span class="sxs-lookup"><span data-stu-id="40257-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="40257-119"><dt>**Copp \_ Proteção 0x7FFFFFF8 \_ reservada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40257-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="40257-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="40257-120">Reserved.</span></span> <span data-ttu-id="40257-121">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="40257-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="40257-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="40257-122">Remarks</span></span>

<span data-ttu-id="40257-123">Alguns métodos retornam um único sinalizador desse tipo de enumeração, e alguns métodos retornam **uma operação OR de um ou mais** sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="40257-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="40257-124">Esses sinalizadores são usados nas consultas e comandos de COPP a seguir.</span><span class="sxs-lookup"><span data-stu-id="40257-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="40257-125">Nível de proteção global</span><span class="sxs-lookup"><span data-stu-id="40257-125">Global Protection Level</span></span>
-   <span data-ttu-id="40257-126">Nível de proteção local</span><span class="sxs-lookup"><span data-stu-id="40257-126">Local Protection Level</span></span>
-   <span data-ttu-id="40257-127">Tipo de proteção</span><span class="sxs-lookup"><span data-stu-id="40257-127">Protection Type</span></span>
-   <span data-ttu-id="40257-128">Definir nível de proteção</span><span class="sxs-lookup"><span data-stu-id="40257-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="40257-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40257-129">Requirements</span></span>



| <span data-ttu-id="40257-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="40257-130">Requirement</span></span> | <span data-ttu-id="40257-131">Valor</span><span class="sxs-lookup"><span data-stu-id="40257-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40257-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40257-132">Header</span></span><br/> | <dl> <span data-ttu-id="40257-133"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="40257-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40257-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="40257-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40257-135">Constantes e GUIDs</span><span class="sxs-lookup"><span data-stu-id="40257-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="40257-136">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="40257-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




