---
description: Se o bit de controle de combinação de combinações for definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático. Isso impede que um usuário insira um novo valor e exige que o usuário escolha apenas um dos valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de controle de combinação de combinações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757526"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="1c1bf-104">Atributo de controle de combinação de combinações</span><span class="sxs-lookup"><span data-stu-id="1c1bf-104">ComboList Control Attribute</span></span>

<span data-ttu-id="1c1bf-105">Se o bit de controle de combinação de combinações for definido em uma caixa de combinação, o campo de edição será substituído por um campo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="1c1bf-106">Isso impede que um usuário insira um novo valor e exige que o usuário escolha apenas um dos valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="1c1bf-107">Se esse bit não estiver definido, a caixa de combinação terá um campo de edição.</span><span class="sxs-lookup"><span data-stu-id="1c1bf-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="1c1bf-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="1c1bf-108">Valid Controls</span></span>

[<span data-ttu-id="1c1bf-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1c1bf-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="1c1bf-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1c1bf-110">Value</span></span>



| <span data-ttu-id="1c1bf-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="1c1bf-111">Decimal</span></span> | <span data-ttu-id="1c1bf-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1c1bf-112">Hexadecimal</span></span> | <span data-ttu-id="1c1bf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c1bf-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="1c1bf-114">131072</span><span class="sxs-lookup"><span data-stu-id="1c1bf-114">131072</span></span>  | <span data-ttu-id="1c1bf-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="1c1bf-115">0x00020000</span></span>  | <span data-ttu-id="1c1bf-116">msidbControlAttributesComboList</span><span class="sxs-lookup"><span data-stu-id="1c1bf-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1c1bf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c1bf-117">Remarks</span></span>

<span data-ttu-id="1c1bf-118">Para definir esse atributo em um controle, inclua o bit de combinação na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c1bf-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="1c1bf-119">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="1c1bf-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



