---
description: A \_ estrutura LARGEINT rotulada define um rótulo que é exibido quando um valor de propriedade LARGEINT específico é detectado.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Estrutura de LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011085"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="7f82c-103">Estrutura de \_ LARGEINT rotulada</span><span class="sxs-lookup"><span data-stu-id="7f82c-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="7f82c-104">A estrutura **\_ LARGEINT rotulada** define um rótulo que é exibido quando um valor de propriedade LARGEINT específico é detectado.</span><span class="sxs-lookup"><span data-stu-id="7f82c-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f82c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f82c-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="7f82c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7f82c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f82c-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7f82c-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="7f82c-108">Valor LARGEINT da propriedade que você deseja detectar.</span><span class="sxs-lookup"><span data-stu-id="7f82c-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="7f82c-109">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="7f82c-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="7f82c-110">Descrição textual ou rótulo que é exibido quando o valor de LARGEINT especificado no membro de **valor** é detectado.</span><span class="sxs-lookup"><span data-stu-id="7f82c-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f82c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f82c-111">Remarks</span></span>

<span data-ttu-id="7f82c-112">O membro **lpLabeledLargeIntTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares de valor LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="7f82c-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="7f82c-113">Os pares são usados quando você deseja exibir um rótulo no lugar de um valor de LARGEINT específico encontrado em um pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7f82c-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f82c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f82c-114">Requirements</span></span>



| <span data-ttu-id="7f82c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f82c-115">Requirement</span></span> | <span data-ttu-id="7f82c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7f82c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f82c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f82c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7f82c-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f82c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f82c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f82c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7f82c-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7f82c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f82c-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f82c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f82c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f82c-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f82c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f82c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f82c-124">SET</span><span class="sxs-lookup"><span data-stu-id="7f82c-124">SET</span></span>](set.md)
</dt> </dl>

 

 




