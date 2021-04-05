---
title: Estrutura de MCI_VCR_PLAY_PARMS (VCR. h)
description: A estrutura do MCI de \_ reprodução de videocassetes \_ \_ contém parâmetros para o \_ comando de reprodução MCI para gravadores de fita de vídeo.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_PLAY_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918557"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="36b6b-104">\_Estrutura de \_ parâmetros de reprodução de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="36b6b-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="36b6b-105">A estrutura do **MCI de \_ \_ reprodução \_ de videocassetes** contém parâmetros para o comando de [**\_ reprodução MCI**](mci-play.md) para gravadores de fita de vídeo.</span><span class="sxs-lookup"><span data-stu-id="36b6b-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b6b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36b6b-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="36b6b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="36b6b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="36b6b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="36b6b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="36b6b-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="36b6b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="36b6b-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="36b6b-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="36b6b-111">Posição da qual reproduzir.</span><span class="sxs-lookup"><span data-stu-id="36b6b-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="36b6b-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="36b6b-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="36b6b-113">Posição para reprodução.</span><span class="sxs-lookup"><span data-stu-id="36b6b-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="36b6b-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="36b6b-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="36b6b-115">Valor de tempo que afeta o comando [**MCI \_ Play**](mci-play.md) ou [**MCI \_ Cue**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="36b6b-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="36b6b-116">Para [**\_ reprodução MCI**](mci-play-parms.md), esse é o momento em que a reprodução é iniciada.</span><span class="sxs-lookup"><span data-stu-id="36b6b-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="36b6b-117">Para **a \_ indicação de MCI**, essa é a hora em que o dispositivo cued atinge a posição fornecida em **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="36b6b-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36b6b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="36b6b-118">Remarks</span></span>

<span data-ttu-id="36b6b-119">As posições são especificadas no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="36b6b-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="36b6b-120">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="36b6b-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b6b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b6b-121">Requirements</span></span>



| <span data-ttu-id="36b6b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b6b-122">Requirement</span></span> | <span data-ttu-id="36b6b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="36b6b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36b6b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b6b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36b6b-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36b6b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36b6b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b6b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36b6b-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36b6b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36b6b-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36b6b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="36b6b-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="36b6b-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36b6b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="36b6b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b6b-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="36b6b-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="36b6b-132">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="36b6b-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="36b6b-133">**indicação de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="36b6b-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="36b6b-134">**\_reprodução MCI**</span><span class="sxs-lookup"><span data-stu-id="36b6b-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="36b6b-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="36b6b-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

