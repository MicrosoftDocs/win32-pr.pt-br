---
title: Estrutura de MCI_VD_PLAY_PARMS (Mciapi. h)
description: A estrutura do MCI \_ \_ reproduzir \_ parâmetros de reprodução contém informações de posição e velocidade para o \_ comando MCI Play para dispositivos VIDEODISC.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Multimídia do Windows da estrutura de MCI_VD_PLAY_PARMS
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009410"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="8f3a5-104">\_Estrutura de \_ parâmetros de reprodução de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="8f3a5-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="8f3a5-105">A estrutura do **MCI \_ \_ reproduzir \_ parâmetros de reprodução** contém informações de posição e velocidade para o comando [**MCI \_ Play**](mci-play.md) para dispositivos VIDEODISC.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3a5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f3a5-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="8f3a5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8f3a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f3a5-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a5-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a5-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a5-111">Posição da qual reproduzir.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a5-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a5-113">Posição para reprodução.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a5-114">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a5-115">Velocidade de reprodução em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f3a5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f3a5-116">Remarks</span></span>

<span data-ttu-id="8f3a5-117">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="8f3a5-118">Você pode usar a estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) em vez de parâmetros de reprodução de VD do MCI se não estiver usando os membros de dados estendidos. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3a5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3a5-119">Requirements</span></span>



| <span data-ttu-id="8f3a5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3a5-120">Requirement</span></span> | <span data-ttu-id="8f3a5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3a5-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3a5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3a5-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f3a5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8f3a5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3a5-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f3a5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f3a5-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f3a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f3a5-127"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3a5-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f3a5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f3a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3a5-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8f3a5-130">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8f3a5-131">**\_reprodução MCI**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="8f3a5-132">**\_parâmetros de reprodução MCI \_**</span><span class="sxs-lookup"><span data-stu-id="8f3a5-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="8f3a5-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f3a5-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

