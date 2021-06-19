---
title: Propriedade Enabled (objeto Command)
description: Saiba mais sobre a propriedade de objeto Comando Habilitado. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407329"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="891f5-104">Propriedade Enabled (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="891f5-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="891f5-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="891f5-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="891f5-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="891f5-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="891f5-107">Retorna ou define se **o Comando** está habilitado no menu pop-up do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="891f5-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="891f5-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="891f5-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="891f5-109">*agent\***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Booliana_ \*  \[  =  *habilitada*\]</span><span class="sxs-lookup"><span data-stu-id="891f5-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="891f5-110">Parte</span><span class="sxs-lookup"><span data-stu-id="891f5-110">Part</span></span>      | <span data-ttu-id="891f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="891f5-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891f5-112">*booleano*</span><span class="sxs-lookup"><span data-stu-id="891f5-112">*boolean*</span></span> | <span data-ttu-id="891f5-113">Uma expressão booliana que especifica se **o Comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="891f5-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="891f5-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadeiro**</dt></span><span class="sxs-lookup"><span data-stu-id="891f5-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="891f5-115">O **Comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="891f5-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="891f5-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt></span><span class="sxs-lookup"><span data-stu-id="891f5-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="891f5-117">O **Comando** está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="891f5-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="891f5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="891f5-118">Remarks</span></span>

<span data-ttu-id="891f5-119">Se a [**propriedade Habilitado**](enabled-property.md) estiver definida [](/windows/desktop/lwef/the-command-object) como **True**, a legenda dos objetos Command aparecerá como texto normal no menu pop-up do caractere quando o aplicativo cliente estiver ativo de entrada.</span><span class="sxs-lookup"><span data-stu-id="891f5-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="891f5-120">Se a **propriedade Enabled** for **False**, a legenda aparecerá como texto indisponível (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="891f5-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="891f5-121">Um Comando **desabilitado** também não está acessível para entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="891f5-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

