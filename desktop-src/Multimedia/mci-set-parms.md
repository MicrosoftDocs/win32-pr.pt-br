---
title: Estrutura de MCI_SET_PARMS (Mciapi. h)
description: A estrutura do MCI \_ set \_ parms contém informações para o \_ comando set do MCI.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- Multimídia do Windows da estrutura de MCI_SET_PARMS
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009056"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="0fd73-104">\_Estrutura do conjunto de parâmetros do MCI \_</span><span class="sxs-lookup"><span data-stu-id="0fd73-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="0fd73-105">A estrutura do **MCI \_ set \_ parms** contém informações para o comando [**\_ set do MCI**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd73-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd73-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fd73-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="0fd73-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0fd73-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fd73-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0fd73-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="0fd73-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0fd73-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0fd73-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-111">Formato de hora para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fd73-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="0fd73-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="0fd73-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="0fd73-113">Canal de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="0fd73-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fd73-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fd73-114">Remarks</span></span>

<span data-ttu-id="0fd73-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="0fd73-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd73-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd73-116">Requirements</span></span>



| <span data-ttu-id="0fd73-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd73-117">Requirement</span></span> | <span data-ttu-id="0fd73-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0fd73-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd73-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fd73-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd73-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fd73-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fd73-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd73-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fd73-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fd73-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0fd73-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd73-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd73-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd73-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd73-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd73-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0fd73-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0fd73-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="0fd73-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0fd73-128">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="0fd73-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="0fd73-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fd73-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

