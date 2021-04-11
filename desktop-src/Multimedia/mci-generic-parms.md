---
title: Estrutura de MCI_GENERIC_PARMS (Mciapi. h)
description: A \_ \_ estrutura de parâmetros genéricos do MCI contém o identificador da janela que recebe mensagens de notificação. Essa estrutura é usada para mensagens de comando MCI que têm listas de parâmetros vazias.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Multimídia do Windows da estrutura de MCI_GENERIC_PARMS
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454984"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="333e5-105">\_Estrutura de parâmetros genéricos do MCI \_</span><span class="sxs-lookup"><span data-stu-id="333e5-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="333e5-106">A estrutura de **\_ \_ parâmetros genéricos do MCI** contém o identificador da janela que recebe mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="333e5-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="333e5-107">Essa estrutura é usada para mensagens de comando MCI que têm listas de parâmetros vazias.</span><span class="sxs-lookup"><span data-stu-id="333e5-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="333e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="333e5-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="333e5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="333e5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="333e5-110">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="333e5-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="333e5-111">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="333e5-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="333e5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="333e5-112">Remarks</span></span>

<span data-ttu-id="333e5-113">As estruturas dos parâmetros de **\_ fechamento \_ MCI** e **MCI \_ percebem \_ parâmetros** são idênticas à estrutura de **\_ \_ parâmetros genéricos do MCI** .</span><span class="sxs-lookup"><span data-stu-id="333e5-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="333e5-114">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="333e5-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="333e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="333e5-115">Requirements</span></span>



| <span data-ttu-id="333e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="333e5-116">Requirement</span></span> | <span data-ttu-id="333e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="333e5-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="333e5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="333e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="333e5-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="333e5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="333e5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="333e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="333e5-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="333e5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="333e5-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="333e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="333e5-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="333e5-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333e5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="333e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333e5-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="333e5-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="333e5-126">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="333e5-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="333e5-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="333e5-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

