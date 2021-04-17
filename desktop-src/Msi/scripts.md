---
description: Uma ação personalizada pode chamar funções que são gravadas em VBScript ou JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760830"
---
# <a name="scripts"></a><span data-ttu-id="fc753-103">Scripts</span><span class="sxs-lookup"><span data-stu-id="fc753-103">Scripts</span></span>

<span data-ttu-id="fc753-104">Uma ação personalizada pode chamar funções que são gravadas em VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="fc753-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="fc753-105">Windows Installer não fornece o mecanismo de script.</span><span class="sxs-lookup"><span data-stu-id="fc753-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="fc753-106">Os autores que desejam usar uma linguagem de script durante a instalação devem, portanto, garantir que o mecanismo de script apropriado esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="fc753-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="fc753-107">O instalador não oferece suporte a JScript versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc753-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="fc753-108">Uma ação personalizada de 64 bits baseada em scripts deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico Actions personalizado na coluna Type da tabela [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc753-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="fc753-109">Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="fc753-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="fc753-110">Os seguintes tipos de ação personalizada básica chamam funções escritas em script.</span><span class="sxs-lookup"><span data-stu-id="fc753-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="fc753-111">Tipo de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="fc753-111">Custom action type</span></span>                                 | <span data-ttu-id="fc753-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc753-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc753-113">Tipo de ação personalizada 5</span><span class="sxs-lookup"><span data-stu-id="fc753-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="fc753-114">Arquivo JScript armazenado em um fluxo de tabela binária.</span><span class="sxs-lookup"><span data-stu-id="fc753-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="fc753-115">Tipo de ação personalizada 21</span><span class="sxs-lookup"><span data-stu-id="fc753-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="fc753-116">Arquivo JScript instalado com um produto.</span><span class="sxs-lookup"><span data-stu-id="fc753-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="fc753-117">Tipo de ação personalizada 53</span><span class="sxs-lookup"><span data-stu-id="fc753-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="fc753-118">Texto JScript especificado por um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc753-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="fc753-119">Tipo de ação personalizada 37</span><span class="sxs-lookup"><span data-stu-id="fc753-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="fc753-120">Texto JScript armazenado na coluna de destino da tabela [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc753-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="fc753-121">Tipo de ação personalizada 6</span><span class="sxs-lookup"><span data-stu-id="fc753-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="fc753-122">Arquivo VBScript armazenado em um fluxo de tabela [binária](binary-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc753-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="fc753-123">Tipo de ação personalizada 22</span><span class="sxs-lookup"><span data-stu-id="fc753-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="fc753-124">Arquivo VBScript instalado com um produto.</span><span class="sxs-lookup"><span data-stu-id="fc753-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="fc753-125">Tipo de ação personalizada 54</span><span class="sxs-lookup"><span data-stu-id="fc753-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="fc753-126">Texto VBScript especificado por um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc753-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="fc753-127">Tipo de ação personalizada 38</span><span class="sxs-lookup"><span data-stu-id="fc753-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="fc753-128">Texto VBScript armazenado na coluna de destino da tabela [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc753-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="fc753-129">O instalador executa ações personalizadas de script diretamente e não usa o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="fc753-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="fc753-130">O objeto **WScript** não pode ser usado dentro de uma ação personalizada de script porque esse objeto é fornecido pelo Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="fc753-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="fc753-131">Os objetos no modelo de objeto do Windows Script Host só poderão ser usados em ações personalizadas se o Windows Script Host estiver instalado no computador criando novas instâncias do objeto, com uma chamada para CreateObject e fornecendo o ProgId do objeto (por exemplo, "WScript. Shell").</span><span class="sxs-lookup"><span data-stu-id="fc753-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="fc753-132">Dependendo do tipo de ação personalizada do script, o acesso a alguns objetos e métodos do modelo de objeto do Windows Script Host pode ser negado por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="fc753-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="fc753-133">Para obter mais informações, consulte [Resumo da lista de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md) para obter um resumo de todos os tipos de ações personalizadas e como eles são codificados na tabela [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fc753-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



