---
title: Estrutura de MCI_VCR_STEP_PARMS (VCR. h)
description: A \_ estrutura de parâmetros de etapa do VCR MCI \_ \_ contém parâmetros para o \_ comando de etapa MCI para gravadores de vídeo-fita.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_STEP_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008979"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="92383-104">\_Estrutura de \_ parâmetros da etapa do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="92383-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="92383-105">A estrutura de **\_ parâmetros de \_ etapa \_ do VCR MCI** contém parâmetros para o comando de [**\_ etapa MCI**](mci-step.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="92383-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="92383-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92383-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="92383-107">Membros</span><span class="sxs-lookup"><span data-stu-id="92383-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="92383-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="92383-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="92383-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="92383-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="92383-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="92383-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="92383-111">Número de quadros para saltar (o comprimento de uma única etapa) conforme as etapas de comando da [**\_ etapa MCI**](mci-step.md) avançam ou regressivem pelo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="92383-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92383-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92383-112">Remarks</span></span>

<span data-ttu-id="92383-113">Ao atribuir dados aos membros nessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="92383-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="92383-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92383-114">Requirements</span></span>



| <span data-ttu-id="92383-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92383-115">Requirement</span></span> | <span data-ttu-id="92383-116">Valor</span><span class="sxs-lookup"><span data-stu-id="92383-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="92383-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92383-117">Minimum supported client</span></span><br/> | <span data-ttu-id="92383-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92383-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="92383-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92383-119">Minimum supported server</span></span><br/> | <span data-ttu-id="92383-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92383-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="92383-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92383-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="92383-122"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="92383-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92383-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="92383-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92383-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="92383-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="92383-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="92383-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="92383-126">**\_etapa MCI**</span><span class="sxs-lookup"><span data-stu-id="92383-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="92383-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92383-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

