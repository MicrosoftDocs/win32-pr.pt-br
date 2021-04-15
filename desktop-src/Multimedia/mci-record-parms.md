---
title: Estrutura de MCI_RECORD_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros do registro MCI \_ contém informações de posicionamento para o \_ comando de registro MCI.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- Multimídia do Windows da estrutura de MCI_RECORD_PARMS
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454603"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="e14fc-104">Estrutura de parâmetros do \_ registro MCI \_</span><span class="sxs-lookup"><span data-stu-id="e14fc-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="e14fc-105">A estrutura de **\_ \_ parâmetros do registro MCI** contém informações de posicionamento para o comando de [**\_ registro MCI**](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="e14fc-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="e14fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e14fc-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="e14fc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e14fc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e14fc-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="e14fc-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="e14fc-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="e14fc-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="e14fc-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="e14fc-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="e14fc-111">Posição da qual reproduzir.</span><span class="sxs-lookup"><span data-stu-id="e14fc-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="e14fc-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="e14fc-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="e14fc-113">Posição para reprodução.</span><span class="sxs-lookup"><span data-stu-id="e14fc-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e14fc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e14fc-114">Remarks</span></span>

<span data-ttu-id="e14fc-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="e14fc-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e14fc-116">Requirements</span></span>



| <span data-ttu-id="e14fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14fc-117">Requirement</span></span> | <span data-ttu-id="e14fc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e14fc-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e14fc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e14fc-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e14fc-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e14fc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e14fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e14fc-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e14fc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e14fc-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e14fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e14fc-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e14fc-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14fc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e14fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14fc-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="e14fc-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e14fc-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="e14fc-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="e14fc-128">**\_registro MCI**</span><span class="sxs-lookup"><span data-stu-id="e14fc-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="e14fc-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e14fc-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

