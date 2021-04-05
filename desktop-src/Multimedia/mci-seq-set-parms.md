---
title: Estrutura de MCI_SEQ_SET_PARMS (Mciapi. h)
description: A estrutura do MCI \_ Seq \_ set \_ parms contém informações para o \_ comando set do MCI para dispositivos do Sequencer MIDI.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Multimídia do Windows da estrutura de MCI_SEQ_SET_PARMS
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918105"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="44f94-104">\_Estrutura do \_ conjunto de \_ parâmetros do MCI Seq</span><span class="sxs-lookup"><span data-stu-id="44f94-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="44f94-105">A estrutura do **MCI \_ Seq \_ set \_ parms** contém informações para o comando [**\_ set do MCI**](mci-set.md) para dispositivos do Sequencer MIDI.</span><span class="sxs-lookup"><span data-stu-id="44f94-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f94-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44f94-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="44f94-107">Membros</span><span class="sxs-lookup"><span data-stu-id="44f94-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="44f94-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="44f94-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="44f94-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="44f94-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-111">Formato de hora do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="44f94-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="44f94-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-113">Canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="44f94-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-114">**dwTempo**</span><span class="sxs-lookup"><span data-stu-id="44f94-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-115">Golpe.</span><span class="sxs-lookup"><span data-stu-id="44f94-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-116">**dwPort**</span><span class="sxs-lookup"><span data-stu-id="44f94-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-117">Porta.</span><span class="sxs-lookup"><span data-stu-id="44f94-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-118">**dwSlave**</span><span class="sxs-lookup"><span data-stu-id="44f94-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-119">Tipo de sincronização usado pelo Sequencer para a operação subordinada.</span><span class="sxs-lookup"><span data-stu-id="44f94-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-120">**dwMaster**</span><span class="sxs-lookup"><span data-stu-id="44f94-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-121">Tipo de sincronização usado pelo Sequencer para a operação mestre.</span><span class="sxs-lookup"><span data-stu-id="44f94-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="44f94-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="44f94-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="44f94-123">Deslocamento de dados.</span><span class="sxs-lookup"><span data-stu-id="44f94-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44f94-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f94-124">Remarks</span></span>

<span data-ttu-id="44f94-125">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="44f94-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f94-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44f94-126">Requirements</span></span>



| <span data-ttu-id="44f94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="44f94-127">Requirement</span></span> | <span data-ttu-id="44f94-128">Valor</span><span class="sxs-lookup"><span data-stu-id="44f94-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44f94-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="44f94-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44f94-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="44f94-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44f94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="44f94-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44f94-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44f94-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44f94-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f94-134"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f94-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44f94-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="44f94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f94-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="44f94-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44f94-137">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="44f94-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="44f94-138">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="44f94-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="44f94-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44f94-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

