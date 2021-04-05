---
description: A estrutura EXPERTFRAMEDESCRIPTOR contém informações sobre um quadro. Quando o especialista chama a função ExpertGetFrame com êxito, Monitor de Rede passa a estrutura EXPERTFRAMEDESCRIPTOR de volta para o especialista.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Estrutura EXPERTFRAMEDESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460964"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="e55ac-104">Estrutura EXPERTFRAMEDESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="e55ac-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="e55ac-105">A estrutura **EXPERTFRAMEDESCRIPTOR** contém informações sobre um quadro.</span><span class="sxs-lookup"><span data-stu-id="e55ac-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="e55ac-106">Quando o especialista chama a função [**ExpertGetFrame**](expertgetframe.md) com êxito, monitor de rede passa a estrutura **EXPERTFRAMEDESCRIPTOR** de volta para o especialista.</span><span class="sxs-lookup"><span data-stu-id="e55ac-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="e55ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e55ac-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="e55ac-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e55ac-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e55ac-109">**FrameNumber**</span><span class="sxs-lookup"><span data-stu-id="e55ac-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e55ac-110">Número de um quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="e55ac-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="e55ac-111">**hFrame**</span><span class="sxs-lookup"><span data-stu-id="e55ac-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="e55ac-112">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="e55ac-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="e55ac-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="e55ac-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="e55ac-114">Ponteiro para um quadro bruto.</span><span class="sxs-lookup"><span data-stu-id="e55ac-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="e55ac-115">**lpRecognizeDataTable**</span><span class="sxs-lookup"><span data-stu-id="e55ac-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="e55ac-116">Tabela que indica onde cada analisador identifica o início dos dados.</span><span class="sxs-lookup"><span data-stu-id="e55ac-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="e55ac-117">**lpPropertyTable**</span><span class="sxs-lookup"><span data-stu-id="e55ac-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="e55ac-118">Tabela de propriedades de quadro que o analisador identifica.</span><span class="sxs-lookup"><span data-stu-id="e55ac-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e55ac-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e55ac-119">Remarks</span></span>

<span data-ttu-id="e55ac-120">Se o especialista especificar \_ as propriedades de anexação de sinalizadores \_ ao chamar [**ExpertGetFrame**](expertgetframe.md), o membro **szPropertyText** em cada estrutura [**PROPERTYINST**](propertyinst.md) será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e55ac-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="e55ac-121">Se o especialista não especificar \_ \_ as propriedades de anexação de sinalizadores ao chamar a função [**ExpertGetFrame**](expertgetframe.md) , o membro **lpPropertyTable** será **nulo** no retorno.</span><span class="sxs-lookup"><span data-stu-id="e55ac-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="e55ac-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e55ac-122">Requirements</span></span>



| <span data-ttu-id="e55ac-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e55ac-123">Requirement</span></span> | <span data-ttu-id="e55ac-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e55ac-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e55ac-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e55ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e55ac-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e55ac-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e55ac-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e55ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e55ac-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e55ac-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e55ac-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e55ac-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e55ac-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e55ac-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




