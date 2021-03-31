---
description: Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que foram compiladas para sistemas de 32 bits ou de 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Ações personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662075"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="9a632-103">Ações personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="9a632-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="9a632-104">Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que foram compiladas para sistemas de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9a632-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="9a632-105">Uma ação personalizada de 64 bits baseada em [scripts](scripts.md) deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico Actions personalizado na coluna Type da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="9a632-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="9a632-106">Constante</span><span class="sxs-lookup"><span data-stu-id="9a632-106">Constant</span></span>                             | <span data-ttu-id="9a632-107">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="9a632-107">Hexadecimal</span></span> | <span data-ttu-id="9a632-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="9a632-108">Decimal</span></span> | <span data-ttu-id="9a632-109">Significado</span><span class="sxs-lookup"><span data-stu-id="9a632-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="9a632-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9a632-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9a632-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="9a632-111">0x0001000</span></span>   | <span data-ttu-id="9a632-112">4096</span><span class="sxs-lookup"><span data-stu-id="9a632-112">4096</span></span>    | <span data-ttu-id="9a632-113">Esta é uma ação personalizada de 64 bits escrita em [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9a632-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="9a632-114">Ações personalizadas com base em [arquivos executáveis](executable-files.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) que foram compatíveis com sistemas operacionais de 64 bits não exigem a inclusão desse bit adicional na coluna Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="9a632-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



