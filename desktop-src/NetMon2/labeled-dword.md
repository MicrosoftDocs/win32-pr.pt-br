---
description: A \_ estrutura DWORD rotulada define um rótulo que é exibido quando um valor específico da propriedade DWORD é detectado.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Estrutura de LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170659"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="9d476-103">\_Estrutura DWORD rotulada</span><span class="sxs-lookup"><span data-stu-id="9d476-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="9d476-104">A estrutura **\_ DWORD rotulada** define um rótulo que é exibido quando um valor específico da propriedade DWORD é detectado.</span><span class="sxs-lookup"><span data-stu-id="9d476-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d476-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d476-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="9d476-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9d476-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d476-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9d476-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="9d476-108">Valor DWORD da propriedade que você deseja detectar.</span><span class="sxs-lookup"><span data-stu-id="9d476-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="9d476-109">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="9d476-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="9d476-110">Descrição textual ou rótulo que é exibido quando o valor DWORD especificado no membro **Value** é detectado.</span><span class="sxs-lookup"><span data-stu-id="9d476-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d476-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d476-111">Remarks</span></span>

<span data-ttu-id="9d476-112">O membro **lpLabeledDwordTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="9d476-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="9d476-113">Os pares são usados quando você deseja exibir um rótulo no lugar de um valor DWORD específico encontrado no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9d476-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d476-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d476-114">Requirements</span></span>



| <span data-ttu-id="9d476-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d476-115">Requirement</span></span> | <span data-ttu-id="9d476-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9d476-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d476-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d476-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d476-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d476-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9d476-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d476-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d476-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d476-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d476-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9d476-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d476-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d476-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d476-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d476-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d476-124">SET</span><span class="sxs-lookup"><span data-stu-id="9d476-124">SET</span></span>](set.md)
</dt> </dl>

 

 




