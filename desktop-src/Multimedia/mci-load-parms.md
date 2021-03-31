---
title: Estrutura de MCI_LOAD_PARMS (mmsystem. h)
description: A \_ estrutura de parâmetros de carregamento MCI \_ contém o nome de arquivo a ser carregado para o \_ comando de carregamento MCI.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Multimídia do Windows da estrutura de MCI_LOAD_PARMS
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645011"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="79daa-104">Estrutura de parâmetros de \_ carga MCI \_</span><span class="sxs-lookup"><span data-stu-id="79daa-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="79daa-105">A estrutura de **\_ \_ parâmetros de carregamento MCI** contém o nome de arquivo a ser carregado para o comando de [**\_ carregamento MCI**](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="79daa-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="79daa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79daa-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="79daa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="79daa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="79daa-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="79daa-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="79daa-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="79daa-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="79daa-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="79daa-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="79daa-111">Nome do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="79daa-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79daa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="79daa-112">Remarks</span></span>

<span data-ttu-id="79daa-113">Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.</span><span class="sxs-lookup"><span data-stu-id="79daa-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="79daa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79daa-114">Requirements</span></span>



| <span data-ttu-id="79daa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79daa-115">Requirement</span></span> | <span data-ttu-id="79daa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="79daa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79daa-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79daa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79daa-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="79daa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="79daa-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79daa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79daa-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="79daa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79daa-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="79daa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79daa-122"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="79daa-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79daa-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79daa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79daa-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="79daa-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="79daa-125">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="79daa-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="79daa-126">**\_carga MCI**</span><span class="sxs-lookup"><span data-stu-id="79daa-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="79daa-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79daa-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

