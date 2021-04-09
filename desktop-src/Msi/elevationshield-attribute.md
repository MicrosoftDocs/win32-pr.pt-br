---
description: Esse atributo adiciona o ícone de elevação do controle de conta de usuário (UAC) (ícone de escudo) ao controle de pressão.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Atributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091691"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="e9b08-103">Atributo ElevationShield</span><span class="sxs-lookup"><span data-stu-id="e9b08-103">ElevationShield Attribute</span></span>

<span data-ttu-id="e9b08-104">Esse atributo adiciona o ícone de elevação do [*controle de conta de usuário*](u-gly.md) (UAC) (ícone de escudo) ao controle de [pressão](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="e9b08-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="e9b08-105">Se esse bit estiver definido e a instalação ainda não estiver sendo executada com privilégios [*elevados*](e-gly.md) , o controle de supressão será criado usando o ícone de elevação do UAC ( [*controle de conta de usuário*](u-gly.md) ) (ícone de escudo).</span><span class="sxs-lookup"><span data-stu-id="e9b08-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="e9b08-106">Se esse bit estiver definido e a instalação já estiver sendo executada com privilégios [*elevados*](e-gly.md) , o controle de supressão será criado usando os outros atributos de ícone.</span><span class="sxs-lookup"><span data-stu-id="e9b08-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="e9b08-107">Se esse bit não estiver definido, o controle de supressão será criado usando os outros atributos Icon.</span><span class="sxs-lookup"><span data-stu-id="e9b08-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="e9b08-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="e9b08-108">Valid Controls</span></span>

[<span data-ttu-id="e9b08-109">Botão</span><span class="sxs-lookup"><span data-stu-id="e9b08-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="e9b08-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e9b08-110">Value</span></span>



| <span data-ttu-id="e9b08-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="e9b08-111">Decimal</span></span> | <span data-ttu-id="e9b08-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="e9b08-112">Hexadecimal</span></span> | <span data-ttu-id="e9b08-113">Constante</span><span class="sxs-lookup"><span data-stu-id="e9b08-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="e9b08-114">8388608</span><span class="sxs-lookup"><span data-stu-id="e9b08-114">8388608</span></span> | <span data-ttu-id="e9b08-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="e9b08-115">0x00800000</span></span>  | <span data-ttu-id="e9b08-116">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="e9b08-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



