---
title: Propriedade Enabled (objeto Command)
description: Propriedade Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105790492"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="65205-103">Propriedade Enabled (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="65205-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="65205-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65205-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="65205-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="65205-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="65205-106">Retorna ou define se o **comando** está habilitado no menu pop-up do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="65205-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="65205-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="65205-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="65205-108">\*Agente \***. Caracteres ("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Booliano* habilitado\]</span><span class="sxs-lookup"><span data-stu-id="65205-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="65205-109">Parte</span><span class="sxs-lookup"><span data-stu-id="65205-109">Part</span></span>      | <span data-ttu-id="65205-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="65205-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65205-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="65205-111">*boolean*</span></span> | <span data-ttu-id="65205-112">Uma expressão booliana que especifica se o **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65205-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="65205-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="65205-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="65205-114">O **comando** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65205-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="65205-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="65205-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="65205-116">O **comando** está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="65205-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65205-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="65205-117">Remarks</span></span>

<span data-ttu-id="65205-118">Se a propriedade [**Enabled**](enabled-property.md) for definida como **true**, a legenda dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) aparecerá como texto normal no menu pop-up do caractere quando o aplicativo cliente for Input-active.</span><span class="sxs-lookup"><span data-stu-id="65205-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="65205-119">Se a propriedade **Enabled** for **false**, a legenda aparecerá como texto indisponível (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="65205-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="65205-120">Um **comando** desabilitado também não está acessível para entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="65205-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

