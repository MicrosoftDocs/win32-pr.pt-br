---
title: Estrutura de MCI_OVLY_RECT_PARMS (Mciapi. h)
description: A estrutura do MCI \_ OVLY \_ Rect \_ parms contém informações de posicionamento para o MCI \_ Put e o MCI \_ , onde os comandos para dispositivos de sobreposição de vídeo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_RECT_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454605"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="d3c53-104">Estrutura de parâmetros do MCI \_ OVLY \_ Rect \_</span><span class="sxs-lookup"><span data-stu-id="d3c53-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="d3c53-105">A estrutura do **MCI \_ OVLY \_ Rect \_ parms** contém informações de posicionamento para o MCI [**\_ Put**](mci-put.md) e o [**MCI, \_ onde**](mci-where.md) os comandos para dispositivos de sobreposição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d3c53-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c53-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3c53-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="d3c53-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d3c53-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3c53-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d3c53-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d3c53-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="d3c53-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d3c53-110">**RC**</span><span class="sxs-lookup"><span data-stu-id="d3c53-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="d3c53-111">Retângulo que contém informações de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="d3c53-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="d3c53-112">As estruturas [Rect](/previous-versions//ms536136(v=vs.85)) são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, **RC. Right** contém a largura do retângulo e **RC. Bottom** contém sua altura.</span><span class="sxs-lookup"><span data-stu-id="d3c53-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3c53-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3c53-113">Remarks</span></span>

<span data-ttu-id="d3c53-114">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="d3c53-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c53-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c53-115">Requirements</span></span>



| <span data-ttu-id="d3c53-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c53-116">Requirement</span></span> | <span data-ttu-id="d3c53-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c53-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c53-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c53-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c53-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3c53-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3c53-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3c53-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c53-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3c53-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3c53-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3c53-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c53-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c53-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c53-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3c53-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c53-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c53-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d3c53-126">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c53-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d3c53-127">**\_Put MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c53-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="d3c53-128">**MCI \_ onde**</span><span class="sxs-lookup"><span data-stu-id="d3c53-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="d3c53-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3c53-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d3c53-130">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3c53-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

