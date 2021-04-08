---
title: Constantes de WINBIO_PRESENCE_CHANGE (WinBio \_ Types. h)
description: Descreve os tipos de alterações que podem ocorrer quando o Windows Biometric Framework monitora a presença de indivíduos.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008968"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="3c827-103">Constantes de alteração de \_ presença de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3c827-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="3c827-104">Descreve os tipos de alterações que podem ocorrer quando o Windows Biometric Framework monitora a presença de indivíduos.</span><span class="sxs-lookup"><span data-stu-id="3c827-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="3c827-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="3c827-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="3c827-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c827-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="3c827-107"><dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="3c827-108">O tipo de evento é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3c827-108">The type of event is unknown.</span></span> <span data-ttu-id="3c827-109">Esse valor é usado para a estrutura não inicializada.</span><span class="sxs-lookup"><span data-stu-id="3c827-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="3c827-110"><dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Atualizar \_ tudo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3c827-111">Fornece informações sobre todas as faces atuais no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="3c827-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="3c827-112"><dt>**WINBIO \_ \_Chegada do \_ tipo \_ de alteração de presença**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="3c827-113">Uma nova face entrou no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="3c827-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="3c827-114"><dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Recognize**</dt> . <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="3c827-115">Uma face foi correspondida a um usuário registrado.</span><span class="sxs-lookup"><span data-stu-id="3c827-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="3c827-116"><dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ parte**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="3c827-117">Uma face detectada anteriormente esteve fora do quadro da câmera por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="3c827-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="3c827-118"><dt>**WINBIO \_ Tipo de alteração de presença \_ \_ \_ Track**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="3c827-119">Fornece informações de atualizações sobre a caixa delimitadora e rejeição de valores de detalhes para um subconjunto das faces que estão atualmente no quadro da câmera.</span><span class="sxs-lookup"><span data-stu-id="3c827-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3c827-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c827-120">Requirements</span></span>



| <span data-ttu-id="3c827-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c827-121">Requirement</span></span> | <span data-ttu-id="3c827-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3c827-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c827-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c827-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3c827-124">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3c827-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3c827-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c827-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3c827-126">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3c827-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="3c827-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c827-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c827-128"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="3c827-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





