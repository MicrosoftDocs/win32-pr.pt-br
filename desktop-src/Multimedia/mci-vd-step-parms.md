---
title: Estrutura de MCI_VD_STEP_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de etapa de VD do MCI \_ \_ contém informações para o \_ comando de etapa MCI para dispositivos VIDEODISC.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- Multimídia do Windows da estrutura de MCI_VD_STEP_PARMS
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499386"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="3ba20-104">\_Estrutura de \_ parâmetros da etapa de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="3ba20-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="3ba20-105">A estrutura de parâmetros de etapa de VD do MCI contém informações para o comando de [**\_ etapa MCI**](mci-step.md) para dispositivos VIDEODISC. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ba20-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba20-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ba20-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="3ba20-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3ba20-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ba20-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="3ba20-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3ba20-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="3ba20-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3ba20-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="3ba20-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="3ba20-111">Número de quadros a serem conetapas.</span><span class="sxs-lookup"><span data-stu-id="3ba20-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ba20-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba20-112">Remarks</span></span>

<span data-ttu-id="3ba20-113">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="3ba20-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba20-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba20-114">Requirements</span></span>



| <span data-ttu-id="3ba20-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba20-115">Requirement</span></span> | <span data-ttu-id="3ba20-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba20-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba20-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba20-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba20-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ba20-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ba20-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba20-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba20-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ba20-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ba20-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ba20-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba20-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba20-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba20-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba20-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3ba20-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3ba20-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="3ba20-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3ba20-126">**\_etapa MCI**</span><span class="sxs-lookup"><span data-stu-id="3ba20-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="3ba20-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ba20-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

