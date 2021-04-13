---
title: Constantes de WINBIO_IRIS (WinBio \_ Types. h)
description: Especifique os tipos para reconhecimento de íris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455404"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="df734-103">Constantes da íris de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="df734-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="df734-104">As seguintes constantes são valores de **\_ \_ subtipo biométrico WINBIO** que podem ser usados para especificar os tipos de reconhecimento de íris além do ANSI INCITS 379-2004: "formato de intercâmbio de imagem íris", que não define nenhum valor de olho à esquerda/direita:</span><span class="sxs-lookup"><span data-stu-id="df734-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="df734-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="df734-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="df734-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="df734-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="df734-107"><dt> **\_ Tipo de íris WINBIO \_ \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="df734-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="df734-108">O tipo de íris é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="df734-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="df734-109"><dt> **\_ \_ \_ Olho esquerdo WINBIO íris**</dt> <dt>0xF5</dt></span><span class="sxs-lookup"><span data-stu-id="df734-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="df734-110">O tipo íris é o olho à esquerda.</span><span class="sxs-lookup"><span data-stu-id="df734-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="df734-111"><dt> **\_ \_ \_ Olho direito de WINBIO íris**</dt> <dt>0xF6</dt></span><span class="sxs-lookup"><span data-stu-id="df734-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="df734-112">O tipo íris é o olho certo.</span><span class="sxs-lookup"><span data-stu-id="df734-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="df734-113"><dt>**WINBIO \_ \_ \_ Pos \_ 01 não especificado pela íris**</dt> <dt>0xF7</dt></span><span class="sxs-lookup"><span data-stu-id="df734-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="df734-114">Subtipo associado com o primeiro modelo de um usuário quando apenas um olho é o quadro de câmera e não pode ser determinado se é o olho do usuário para a esquerda ou para a direita.</span><span class="sxs-lookup"><span data-stu-id="df734-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="df734-115"><dt> **WINBIO \_ do \_ PDV não \_ especificado \_ na íris, 02**</dt> <dt>0xF8</dt></span><span class="sxs-lookup"><span data-stu-id="df734-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="df734-116">Subtipo associado a um modelo do usuário s segundo quando apenas um olho é o quadro da câmera e não pode ser determinado se é o olho do usuário para a esquerda ou para a direita.</span><span class="sxs-lookup"><span data-stu-id="df734-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="df734-117"><dt> **WINBIO \_ íris \_ 0xF9 \_ Eyes**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df734-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="df734-118">O tipo íris é ambos os olhos.</span><span class="sxs-lookup"><span data-stu-id="df734-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="df734-119"><dt> **WINBIO \_ íris \_ \_ olho**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="df734-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="df734-120">O tipo de íris é olho.</span><span class="sxs-lookup"><span data-stu-id="df734-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="df734-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df734-121">Requirements</span></span>



| <span data-ttu-id="df734-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df734-122">Requirement</span></span> | <span data-ttu-id="df734-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df734-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df734-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df734-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df734-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="df734-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="df734-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df734-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df734-127">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="df734-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="df734-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df734-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="df734-129"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df734-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





