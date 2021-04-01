---
title: Estrutura de MCI_SEEK_PARMS (Mciapi. h)
description: A estrutura de parâmetros de busca do MCI \_ \_ contém informações de posicionamento para o comando de busca do MCI \_ .
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- Multimídia do Windows da estrutura de MCI_SEEK_PARMS
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644396"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="407c5-104">Estrutura de parâmetros de \_ busca MCI \_</span><span class="sxs-lookup"><span data-stu-id="407c5-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="407c5-105">A estrutura de **\_ \_ parâmetros de busca do MCI** contém informações de posicionamento para o comando de [**\_ busca do MCI**](mci-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="407c5-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="407c5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="407c5-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="407c5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="407c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="407c5-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="407c5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="407c5-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="407c5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="407c5-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="407c5-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="407c5-111">Posição para a qual buscar.</span><span class="sxs-lookup"><span data-stu-id="407c5-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="407c5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="407c5-112">Remarks</span></span>

<span data-ttu-id="407c5-113">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="407c5-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="407c5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407c5-114">Requirements</span></span>



| <span data-ttu-id="407c5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="407c5-115">Requirement</span></span> | <span data-ttu-id="407c5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="407c5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="407c5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="407c5-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="407c5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="407c5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="407c5-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="407c5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="407c5-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="407c5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="407c5-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="407c5-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="407c5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="407c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407c5-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="407c5-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="407c5-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="407c5-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="407c5-126">**busca de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="407c5-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="407c5-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="407c5-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

