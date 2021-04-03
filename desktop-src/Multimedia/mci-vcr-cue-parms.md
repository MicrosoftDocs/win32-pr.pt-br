---
title: Estrutura de MCI_VCR_CUE_PARMS (VCR. h)
description: A estrutura de parâmetros de indicação de VCR do MCI \_ \_ \_ contém parâmetros para o \_ comando de indicação MCI para gravadores de vídeo-fita.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_CUE_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824736"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="bc637-104">\_Estrutura de \_ parâmetros de sinalização VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="bc637-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="bc637-105">A estrutura de parâmetros de indicação de VCR do MCI contém parâmetros para o comando de [**\_ indicação MCI**](mci-cue.md) para gravadores de vídeo-fita. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc637-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc637-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc637-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="bc637-107">Membros</span><span class="sxs-lookup"><span data-stu-id="bc637-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc637-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="bc637-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bc637-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="bc637-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bc637-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="bc637-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="bc637-111">Posição da qual se deve se marcar.</span><span class="sxs-lookup"><span data-stu-id="bc637-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="bc637-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="bc637-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="bc637-113">Posição para indicação.</span><span class="sxs-lookup"><span data-stu-id="bc637-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc637-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc637-114">Remarks</span></span>

<span data-ttu-id="bc637-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="bc637-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc637-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc637-116">Requirements</span></span>



| <span data-ttu-id="bc637-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc637-117">Requirement</span></span> | <span data-ttu-id="bc637-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bc637-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bc637-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc637-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc637-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc637-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bc637-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc637-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc637-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc637-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc637-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc637-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc637-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc637-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc637-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc637-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc637-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bc637-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc637-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="bc637-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bc637-128">**indicação de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="bc637-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="bc637-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc637-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

