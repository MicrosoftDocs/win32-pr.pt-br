---
title: Estrutura de MCI_VCR_STATUS_PARMS (VCR. h)
description: A estrutura do parâmetro de \_ status do VCR MCI \_ \_ contém parâmetros para o comando de status do MCI \_ para gravadores de vídeo-fita.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_STATUS_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918056"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="6463f-104">\_Estrutura de \_ parâmetros de status do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="6463f-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="6463f-105">A estrutura do parâmetro de **\_ status do VCR \_ \_ MCI** contém parâmetros para o comando de [**\_ status do MCI**](mci-status.md) para gravadores de vídeo-fita.</span><span class="sxs-lookup"><span data-stu-id="6463f-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="6463f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6463f-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="6463f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6463f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6463f-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6463f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6463f-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="6463f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6463f-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="6463f-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="6463f-111">Valor retornado pelo comando [**\_ status do MCI**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="6463f-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="6463f-112">O valor de retorno varia de acordo com a consulta do comando.</span><span class="sxs-lookup"><span data-stu-id="6463f-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="6463f-113">Para obter mais informações, consulte a descrição do [**comando \_ status do MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6463f-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6463f-114">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="6463f-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="6463f-115">Tipo de informação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6463f-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="6463f-116">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="6463f-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="6463f-117">Faixa de áudio ou vídeo que armazenará informações durante a próxima gravação.</span><span class="sxs-lookup"><span data-stu-id="6463f-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="6463f-118">Esse membro é usado para retornar informações quando o [**comando \_ status do MCI**](mci-status-parms.md) questiona sobre o status de gravação de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="6463f-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="6463f-119">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="6463f-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6463f-120">Sintonizador lógico ao qual o canal atual está associado.</span><span class="sxs-lookup"><span data-stu-id="6463f-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="6463f-121">Esse membro é usado para retornar informações quando o [**comando \_ status do MCI**](mci-status.md) questiona sobre o número do canal atual.</span><span class="sxs-lookup"><span data-stu-id="6463f-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6463f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6463f-122">Remarks</span></span>

<span data-ttu-id="6463f-123">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="6463f-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6463f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6463f-124">Requirements</span></span>



| <span data-ttu-id="6463f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6463f-125">Requirement</span></span> | <span data-ttu-id="6463f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6463f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6463f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6463f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6463f-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6463f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6463f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6463f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6463f-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6463f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6463f-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6463f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6463f-132"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="6463f-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6463f-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6463f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6463f-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6463f-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6463f-135">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="6463f-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6463f-136">**STATUS do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="6463f-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="6463f-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6463f-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

