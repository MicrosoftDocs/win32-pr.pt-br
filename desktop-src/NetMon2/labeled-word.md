---
description: A estrutura de \_ palavras rotulada define um rótulo que é exibido quando um valor de propriedade de palavra específico é detectado.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Estrutura de LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754315"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="47013-103">Estrutura de \_ palavras rotulada</span><span class="sxs-lookup"><span data-stu-id="47013-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="47013-104">A estrutura de **\_ palavras rotulada** define um rótulo que é exibido quando um valor de propriedade de palavra específico é detectado.</span><span class="sxs-lookup"><span data-stu-id="47013-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="47013-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47013-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="47013-106">Membros</span><span class="sxs-lookup"><span data-stu-id="47013-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="47013-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="47013-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="47013-108">Valor de palavra da propriedade que você deseja detectar.</span><span class="sxs-lookup"><span data-stu-id="47013-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="47013-109">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="47013-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="47013-110">Descrição textual ou rótulo que é exibido quando o valor de palavra especificado no membro de **valor** é detectado.</span><span class="sxs-lookup"><span data-stu-id="47013-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47013-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="47013-111">Remarks</span></span>

<span data-ttu-id="47013-112">O membro **lpLabeledWordTable** da estrutura [set](set.md) aponta para uma matriz de estruturas set para definir um ou mais pares rótulo Value.</span><span class="sxs-lookup"><span data-stu-id="47013-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="47013-113">Esses pares são usados quando você deseja exibir um rótulo no lugar de um valor de palavra específico encontrado em um pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="47013-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="47013-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47013-114">Requirements</span></span>



| <span data-ttu-id="47013-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="47013-115">Requirement</span></span> | <span data-ttu-id="47013-116">Valor</span><span class="sxs-lookup"><span data-stu-id="47013-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="47013-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47013-117">Minimum supported client</span></span><br/> | <span data-ttu-id="47013-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47013-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="47013-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47013-119">Minimum supported server</span></span><br/> | <span data-ttu-id="47013-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47013-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="47013-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="47013-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="47013-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="47013-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47013-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="47013-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47013-124">SET</span><span class="sxs-lookup"><span data-stu-id="47013-124">SET</span></span>](set.md)
</dt> </dl>

 

 




