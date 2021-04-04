---
title: Estrutura de MCI_STATUS_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros de status MCI \_ contém informações para o \_ comando status MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Multimídia do Windows da estrutura de MCI_STATUS_PARMS
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918104"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="98c11-104">Estrutura de parâmetros de \_ status do MCI \_</span><span class="sxs-lookup"><span data-stu-id="98c11-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="98c11-105">A estrutura de **\_ \_ parâmetros de status MCI** contém informações para o comando [**\_ status MCI**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="98c11-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c11-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98c11-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="98c11-107">Membros</span><span class="sxs-lookup"><span data-stu-id="98c11-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="98c11-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="98c11-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="98c11-109">A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.</span><span class="sxs-lookup"><span data-stu-id="98c11-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="98c11-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="98c11-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="98c11-111">Contém informações sobre o retorno.</span><span class="sxs-lookup"><span data-stu-id="98c11-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="98c11-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="98c11-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="98c11-113">Funcionalidade que está sendo consultada.</span><span class="sxs-lookup"><span data-stu-id="98c11-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="98c11-114">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="98c11-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="98c11-115">Comprimento ou número de faixas.</span><span class="sxs-lookup"><span data-stu-id="98c11-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98c11-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="98c11-116">Remarks</span></span>

<span data-ttu-id="98c11-117">O \_ sinalizador de item de status MCI \_ deve ser definido no parâmetro *FdwCommand* da função [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar o membro **dwItem** , que deve conter uma das constantes que indicam quais informações de status estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="98c11-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c11-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c11-118">Requirements</span></span>



| <span data-ttu-id="98c11-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c11-119">Requirement</span></span> | <span data-ttu-id="98c11-120">Valor</span><span class="sxs-lookup"><span data-stu-id="98c11-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98c11-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="98c11-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98c11-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="98c11-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="98c11-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98c11-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="98c11-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="98c11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c11-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c11-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c11-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="98c11-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c11-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="98c11-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="98c11-129">**Estruturas MCI**</span><span class="sxs-lookup"><span data-stu-id="98c11-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="98c11-130">**STATUS do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="98c11-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="98c11-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="98c11-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

