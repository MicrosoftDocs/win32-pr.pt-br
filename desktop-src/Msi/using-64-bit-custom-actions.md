---
description: Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que são compiladas para sistemas de 32 bits ou de 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Usando ações personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922128"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="002b1-103">Usando ações personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="002b1-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="002b1-104">Em sistemas operacionais de 64 bits, Windows Installer pode chamar ações personalizadas que são compiladas para sistemas de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="002b1-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="002b1-105">Uma ação personalizada de 64 bits baseada em [scripts](scripts.md) deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico de ação personalizada na coluna tipo da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="002b1-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="002b1-106">Ações personalizadas com base em [arquivos executáveis](executable-files.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) que são compatíveis com sistemas operacionais de 64 bits não exigem a inclusão desse bit adicional na coluna Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="002b1-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="002b1-107">Para obter mais informações, consulte [ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="002b1-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 



