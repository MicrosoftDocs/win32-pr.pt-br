---
title: Estrutura de MCI_BREAK_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de interrupção MCI contém o código de \_ chave virtual e as informações de janela do \_ comando MCI Break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Multimídia do Windows da estrutura de MCI_BREAK_PARMS
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499325"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="005b4-104">Estrutura de parâmetros de \_ interrupção MCI \_</span><span class="sxs-lookup"><span data-stu-id="005b4-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="005b4-105">A estrutura de **\_ \_ parâmetros de interrupção MCI** contém o código de chave virtual e as informações de janela do comando [**MCI \_ Break**](mci-break.md) .</span><span class="sxs-lookup"><span data-stu-id="005b4-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="005b4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="005b4-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="005b4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="005b4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="005b4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="005b4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="005b4-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="005b4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="005b4-110">**nVirtKey**</span><span class="sxs-lookup"><span data-stu-id="005b4-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="005b4-111">Código de chave virtual para chave de interrupção.</span><span class="sxs-lookup"><span data-stu-id="005b4-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="005b4-112">**hwndBreak**</span><span class="sxs-lookup"><span data-stu-id="005b4-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="005b4-113">Identificador para a janela que deve ser a janela atual para detecção de interrupção.</span><span class="sxs-lookup"><span data-stu-id="005b4-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="005b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="005b4-114">Remarks</span></span>

<span data-ttu-id="005b4-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="005b4-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="005b4-116">Os seguintes sinalizadores são definidos:</span><span class="sxs-lookup"><span data-stu-id="005b4-116">The following flags are defined:</span></span>

<span data-ttu-id="005b4-117">\_HWND de interrupção de MCI \_</span><span class="sxs-lookup"><span data-stu-id="005b4-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="005b4-118">Valida o membro **hwndBreak** especificando a janela que deve ter foco para habilitar a detecção de interrupção.</span><span class="sxs-lookup"><span data-stu-id="005b4-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="005b4-119">\_chave de interrupção MCI \_</span><span class="sxs-lookup"><span data-stu-id="005b4-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="005b4-120">Valida o membro **nVirtKey** especificando o código de chave virtual a ser usado para a chave de interrupção.</span><span class="sxs-lookup"><span data-stu-id="005b4-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="005b4-121">interrupção do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="005b4-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="005b4-122">Desabilita qualquer chave de quebra existente.</span><span class="sxs-lookup"><span data-stu-id="005b4-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="005b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="005b4-123">Requirements</span></span>



| <span data-ttu-id="005b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="005b4-124">Requirement</span></span> | <span data-ttu-id="005b4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="005b4-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="005b4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="005b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="005b4-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="005b4-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="005b4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="005b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="005b4-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="005b4-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="005b4-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="005b4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="005b4-131"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="005b4-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005b4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="005b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005b4-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="005b4-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="005b4-134">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="005b4-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="005b4-135">**interrupção de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="005b4-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="005b4-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="005b4-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

