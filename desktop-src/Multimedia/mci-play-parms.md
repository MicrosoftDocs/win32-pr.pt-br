---
title: Estrutura de MCI_PLAY_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de reprodução MCI \_ contém informações de posicionamento para o \_ comando de reprodução MCI.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- Multimídia do Windows da estrutura de MCI_PLAY_PARMS
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917970"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="e6617-104">Estrutura de parâmetros de \_ reprodução MCI \_</span><span class="sxs-lookup"><span data-stu-id="e6617-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="e6617-105">A estrutura de **\_ \_ parâmetros de reprodução MCI** contém informações de posicionamento para o comando de [**\_ reprodução MCI**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="e6617-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6617-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6617-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="e6617-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e6617-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6617-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="e6617-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="e6617-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="e6617-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="e6617-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="e6617-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="e6617-111">Posição da qual reproduzir.</span><span class="sxs-lookup"><span data-stu-id="e6617-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="e6617-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="e6617-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="e6617-113">Posição para reprodução.</span><span class="sxs-lookup"><span data-stu-id="e6617-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6617-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6617-114">Remarks</span></span>

<span data-ttu-id="e6617-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="e6617-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6617-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6617-116">Requirements</span></span>



| <span data-ttu-id="e6617-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6617-117">Requirement</span></span> | <span data-ttu-id="e6617-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e6617-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6617-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6617-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6617-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6617-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6617-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6617-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6617-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6617-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6617-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6617-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6617-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6617-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6617-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6617-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6617-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="e6617-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6617-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="e6617-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="e6617-128">**\_reprodução MCI**</span><span class="sxs-lookup"><span data-stu-id="e6617-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="e6617-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6617-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

