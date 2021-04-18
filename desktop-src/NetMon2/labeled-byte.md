---
description: A estrutura de \_ bytes rotulada define um par de bits rotulado. O rótulo do par de bits rotulado é exibido quando um valor de propriedade de byte específico é detectado.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Estrutura de LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752232"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="b9859-104">Estrutura de \_ bytes rotulada</span><span class="sxs-lookup"><span data-stu-id="b9859-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="b9859-105">A estrutura de **\_ bytes rotulada** define um par de bits rotulado.</span><span class="sxs-lookup"><span data-stu-id="b9859-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="b9859-106">O **rótulo** do par de bits rotulado é exibido quando um valor de propriedade de byte específico é detectado.</span><span class="sxs-lookup"><span data-stu-id="b9859-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9859-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9859-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="b9859-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b9859-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9859-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b9859-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="b9859-110">Valor de BYTE da propriedade que você deseja detectar.</span><span class="sxs-lookup"><span data-stu-id="b9859-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="b9859-111">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="b9859-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="b9859-112">Descrição textual ou rótulo que é exibido quando o valor especificado no membro de **valor** é detectado.</span><span class="sxs-lookup"><span data-stu-id="b9859-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9859-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9859-113">Remarks</span></span>

<span data-ttu-id="b9859-114">O membro **lpLabeledByteTable** da estrutura [set](set.md) aponta para uma matriz de estruturas **set** que definem um ou mais membros **Label** dos pares de valor de byte.</span><span class="sxs-lookup"><span data-stu-id="b9859-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="b9859-115">Esses pares são usados quando você deseja exibir um rótulo no lugar de um valor de BYTE específico encontrado no pacote de protocolo.</span><span class="sxs-lookup"><span data-stu-id="b9859-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9859-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9859-116">Requirements</span></span>



| <span data-ttu-id="b9859-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9859-117">Requirement</span></span> | <span data-ttu-id="b9859-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b9859-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9859-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9859-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9859-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9859-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9859-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9859-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9859-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9859-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b9859-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b9859-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9859-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9859-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9859-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9859-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9859-126">SET</span><span class="sxs-lookup"><span data-stu-id="b9859-126">SET</span></span>](set.md)
</dt> </dl>

 

 




