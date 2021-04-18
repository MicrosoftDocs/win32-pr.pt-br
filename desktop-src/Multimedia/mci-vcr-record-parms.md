---
title: Estrutura de MCI_VCR_RECORD_PARMS (VCR. h)
description: A estrutura de parâmetros de \_ registro de VCR MCI \_ \_ contém parâmetros para o \_ comando de registro MCI para gravadores de vídeo-fita.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_RECORD_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759200"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="3a641-104">\_Estrutura de \_ parâmetros de registro de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="3a641-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="3a641-105">A estrutura de parâmetros de **\_ registro de VCR \_ \_ MCI** contém parâmetros para o comando de [**\_ registro MCI**](mci-record.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="3a641-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a641-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a641-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="3a641-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3a641-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a641-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="3a641-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3a641-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="3a641-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3a641-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="3a641-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="3a641-111">Posição da qual reproduzir.</span><span class="sxs-lookup"><span data-stu-id="3a641-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="3a641-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="3a641-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="3a641-113">Posição para reprodução.</span><span class="sxs-lookup"><span data-stu-id="3a641-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="3a641-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="3a641-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="3a641-115">Valor de tempo que afeta [**o \_ registro MCI**](mci-record.md) ou o comando de [**\_ indicação MCI**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="3a641-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="3a641-116">Para **o \_ registro MCI**, esse é o momento em que a gravação começa.</span><span class="sxs-lookup"><span data-stu-id="3a641-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="3a641-117">Para **a \_ indicação de MCI**, essa é a hora em que o dispositivo cued atinge a posição fornecida em **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="3a641-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a641-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a641-118">Remarks</span></span>

<span data-ttu-id="3a641-119">As posições são especificadas no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="3a641-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="3a641-120">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="3a641-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a641-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a641-121">Requirements</span></span>



| <span data-ttu-id="3a641-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a641-122">Requirement</span></span> | <span data-ttu-id="3a641-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3a641-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a641-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a641-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a641-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a641-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3a641-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a641-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a641-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a641-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a641-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a641-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a641-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a641-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a641-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a641-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a641-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3a641-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3a641-132">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="3a641-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3a641-133">**indicação de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="3a641-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="3a641-134">**\_registro MCI**</span><span class="sxs-lookup"><span data-stu-id="3a641-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="3a641-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a641-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

