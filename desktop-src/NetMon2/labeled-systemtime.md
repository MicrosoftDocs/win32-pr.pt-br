---
description: A \_ estrutura SYSTEMTIME rotulada define um rótulo que é exibido quando um valor de Propriedade SYSTEMTIME específico é detectado.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Estrutura de LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837293"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="f41a4-103">Estrutura de \_ SYSTEMTIME rotulada</span><span class="sxs-lookup"><span data-stu-id="f41a4-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="f41a4-104">A estrutura **\_ SYSTEMTIME rotulada** define um rótulo que é exibido quando um valor de Propriedade SYSTEMTIME específico é detectado.</span><span class="sxs-lookup"><span data-stu-id="f41a4-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="f41a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f41a4-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="f41a4-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f41a4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f41a4-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f41a4-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="f41a4-108">Valor SYSTEMTIME de uma propriedade que você deseja detectar.</span><span class="sxs-lookup"><span data-stu-id="f41a4-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="f41a4-109">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="f41a4-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="f41a4-110">Descrição textual ou rótulo que é exibido quando o valor de SYSTEMTIME especificado no membro de **valor** é detectado.</span><span class="sxs-lookup"><span data-stu-id="f41a4-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f41a4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f41a4-111">Remarks</span></span>

<span data-ttu-id="f41a4-112">O membro **lpLabeledSystemTimeTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais pares rótulo Value.</span><span class="sxs-lookup"><span data-stu-id="f41a4-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="f41a4-113">Os pares são usados quando você deseja exibir um rótulo no lugar de um valor de LARGEINT específico que é encontrado no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f41a4-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="f41a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f41a4-114">Requirements</span></span>



| <span data-ttu-id="f41a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f41a4-115">Requirement</span></span> | <span data-ttu-id="f41a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f41a4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f41a4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f41a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f41a4-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f41a4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f41a4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f41a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f41a4-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f41a4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f41a4-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f41a4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f41a4-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f41a4-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f41a4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f41a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f41a4-124">SET</span><span class="sxs-lookup"><span data-stu-id="f41a4-124">SET</span></span>](set.md)
</dt> </dl>

 

 




