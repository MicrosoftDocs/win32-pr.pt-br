---
title: Estrutura de MCI_WAVE_DELETE_PARMS (Mciapi. h)
description: A estrutura de parâmetros de exclusão de Wave do MCI \_ \_ \_ contém informações de posição para o \_ comando MCI Delete para dispositivos de forma de onda-áudio.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Multimídia do Windows da estrutura de MCI_WAVE_DELETE_PARMS
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454802"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="ce076-104">\_Estrutura de \_ parâmetros de exclusão de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="ce076-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="ce076-105">A estrutura de parâmetros de exclusão de Wave do MCI contém informações de posição para o comando [**MCI \_ delete**](mci-delete.md) para dispositivos de forma de onda-áudio. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce076-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce076-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce076-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="ce076-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ce076-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce076-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ce076-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ce076-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="ce076-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ce076-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="ce076-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="ce076-111">Posição da qual excluir.</span><span class="sxs-lookup"><span data-stu-id="ce076-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="ce076-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="ce076-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="ce076-113">Posição para a qual excluir.</span><span class="sxs-lookup"><span data-stu-id="ce076-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce076-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce076-114">Remarks</span></span>

<span data-ttu-id="ce076-115">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="ce076-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce076-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce076-116">Requirements</span></span>



| <span data-ttu-id="ce076-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce076-117">Requirement</span></span> | <span data-ttu-id="ce076-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ce076-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce076-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce076-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce076-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce076-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ce076-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce076-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce076-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce076-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce076-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ce076-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce076-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce076-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce076-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce076-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce076-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ce076-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ce076-127">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="ce076-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ce076-128">**exclusão de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ce076-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="ce076-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce076-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

