---
description: A estrutura de \_ bits rotulada define um par de bits de rótulo.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Estrutura de LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750207"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="51bfa-103">Estrutura de \_ bits rotulada</span><span class="sxs-lookup"><span data-stu-id="51bfa-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="51bfa-104">A estrutura de **\_ bits rotulada** define um par de bits de rótulo.</span><span class="sxs-lookup"><span data-stu-id="51bfa-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bfa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51bfa-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="51bfa-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51bfa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51bfa-107">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="51bfa-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="51bfa-108">Número de bits do par de bits de rótulo.</span><span class="sxs-lookup"><span data-stu-id="51bfa-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="51bfa-109">Os valores variam de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="51bfa-109">Values range from 0 to 255.</span></span> <span data-ttu-id="51bfa-110">Defina o membro **Bitnumber** como o bit usado na comparação do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="51bfa-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="51bfa-111">**LabelOff**</span><span class="sxs-lookup"><span data-stu-id="51bfa-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="51bfa-112">Cadeia de caracteres ou rótulo exibido quando o BIT especificado em **BitNumber** é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="51bfa-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="51bfa-113">Por exemplo, um rótulo possível é "bit desativado".</span><span class="sxs-lookup"><span data-stu-id="51bfa-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="51bfa-114">**Rotular**</span><span class="sxs-lookup"><span data-stu-id="51bfa-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="51bfa-115">Cadeia de caracteres ou rótulo exibido quando o BIT especificado em **BitNumber** é igual a 1.</span><span class="sxs-lookup"><span data-stu-id="51bfa-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="51bfa-116">Por exemplo, um rótulo possível é "bit em".</span><span class="sxs-lookup"><span data-stu-id="51bfa-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51bfa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51bfa-117">Remarks</span></span>

<span data-ttu-id="51bfa-118">Uma matriz de estruturas de **\_ bits rotuladas** é usada para definir um conjunto de pares de bits de rótulo.</span><span class="sxs-lookup"><span data-stu-id="51bfa-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="51bfa-119">Um ponteiro para a matriz é especificado no membro **lpLabeledBit** da estrutura [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="51bfa-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="51bfa-120">Os pares são usados quando você deseja exibir um rótulo com base na configuração de cada BIT.</span><span class="sxs-lookup"><span data-stu-id="51bfa-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="51bfa-121">Normalmente, esse tipo de conjunto é usado para indicar o valor de ON ou OFF de BITs.</span><span class="sxs-lookup"><span data-stu-id="51bfa-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="51bfa-122">Quando um conjunto de bits é especificado, Monitor de Rede exibe somente os BITs incluídos na matriz de estruturas de **conjunto** .</span><span class="sxs-lookup"><span data-stu-id="51bfa-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="51bfa-123">BITs que não estão na estrutura **definida** não são exibidos.</span><span class="sxs-lookup"><span data-stu-id="51bfa-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bfa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51bfa-124">Requirements</span></span>



| <span data-ttu-id="51bfa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51bfa-125">Requirement</span></span> | <span data-ttu-id="51bfa-126">Valor</span><span class="sxs-lookup"><span data-stu-id="51bfa-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51bfa-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bfa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="51bfa-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51bfa-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51bfa-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bfa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="51bfa-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51bfa-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51bfa-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51bfa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="51bfa-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51bfa-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51bfa-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="51bfa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bfa-134">SET</span><span class="sxs-lookup"><span data-stu-id="51bfa-134">SET</span></span>](set.md)
</dt> </dl>

 

 




