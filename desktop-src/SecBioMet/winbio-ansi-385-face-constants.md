---
title: Constantes de WINBIO_ANSI_385_FACE (WinBio \_ Types. h)
description: Especifique os tipos de imagem de face frontais para reconhecimento facial.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086133"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="e0014-103">Constantes de face do WINBIO \_ ANSI \_ 385 \_</span><span class="sxs-lookup"><span data-stu-id="e0014-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="e0014-104">As seguintes constantes são valores de **\_ \_ subtipo biométrico WINBIO** que podem ser usados para especificar os dois tipos de imagens de face frontais, conforme definido pelo ANSI INCITS 385-2004: "formato de reconhecimento facial para intercâmbio de dados": resolução completa e baixa resolução.</span><span class="sxs-lookup"><span data-stu-id="e0014-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="e0014-105">Na prática, a estrutura biométrica usará apenas imagens de resolução completa para reconhecimento facial.</span><span class="sxs-lookup"><span data-stu-id="e0014-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="e0014-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e0014-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="e0014-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0014-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="e0014-108"><dt>**WINBIO \_ \_Tipo de \_ FACE ANSI 385 \_ \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0014-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="e0014-109">O tipo de imagem de face frontais é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e0014-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="e0014-110"><dt>**WINBIO \_ ANSI \_ 385 \_ face \_ frontais \_ Full**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e0014-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="e0014-111">O tipo de imagem de face frontais é resolução completa.</span><span class="sxs-lookup"><span data-stu-id="e0014-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="e0014-112"><dt>**WINBIO \_ \_Símbolo de \_ \_ frontais de \_ face ANSI 385**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e0014-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e0014-113">O tipo de imagem de face frontais é de baixa resolução.</span><span class="sxs-lookup"><span data-stu-id="e0014-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="e0014-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0014-114">Requirements</span></span>



| <span data-ttu-id="e0014-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0014-115">Requirement</span></span> | <span data-ttu-id="e0014-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e0014-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0014-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0014-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0014-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e0014-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e0014-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0014-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0014-120">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e0014-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e0014-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0014-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0014-122"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0014-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





