---
title: Estrutura de MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: A estrutura do MCI \_ GETDEVCAPS \_ parms contém informações de capacidade de dispositivo para o \_ comando GETDEVCAPS MCI.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Multimídia do Windows da estrutura de MCI_GETDEVCAPS_PARMS
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009061"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="ecd59-104">\_Estrutura do GETDEVCAPS \_ parms de MCI</span><span class="sxs-lookup"><span data-stu-id="ecd59-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="ecd59-105">A estrutura do **MCI \_ GETDEVCAPS \_ parms** contém informações de capacidade de dispositivo para o comando [**\_ GETDEVCAPS MCI**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd59-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd59-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecd59-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="ecd59-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ecd59-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecd59-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ecd59-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ecd59-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="ecd59-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ecd59-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="ecd59-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="ecd59-111">Contém informações sobre a saída.</span><span class="sxs-lookup"><span data-stu-id="ecd59-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="ecd59-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="ecd59-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="ecd59-113">Funcionalidade que está sendo consultada.</span><span class="sxs-lookup"><span data-stu-id="ecd59-113">Capability being queried.</span></span> <span data-ttu-id="ecd59-114">Esse membro pode ser uma das constantes listadas no material de referência para o comando [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd59-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecd59-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecd59-115">Remarks</span></span>

<span data-ttu-id="ecd59-116">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="ecd59-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd59-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecd59-117">Requirements</span></span>



| <span data-ttu-id="ecd59-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd59-118">Requirement</span></span> | <span data-ttu-id="ecd59-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ecd59-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd59-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecd59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd59-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecd59-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ecd59-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecd59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd59-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecd59-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ecd59-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ecd59-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd59-125"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd59-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd59-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecd59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd59-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ecd59-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ecd59-128">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="ecd59-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ecd59-129">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="ecd59-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="ecd59-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ecd59-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

