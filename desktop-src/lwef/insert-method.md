---
title: Método Insert
description: Método Insert
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105779337"
---
# <a name="insert-method"></a><span data-ttu-id="eb943-103">Método Insert</span><span class="sxs-lookup"><span data-stu-id="eb943-103">Insert Method</span></span>

<span data-ttu-id="eb943-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb943-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eb943-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="eb943-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eb943-106">Insere um objeto de **comando** na coleção de **comandos** .</span><span class="sxs-lookup"><span data-stu-id="eb943-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="eb943-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="eb943-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eb943-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Comandos. Insert* \*  *nome*, *refname*, *antes*\_</span><span class="sxs-lookup"><span data-stu-id="eb943-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="eb943-109">*Legenda*, *voz, habilitada, visível*</span><span class="sxs-lookup"><span data-stu-id="eb943-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="eb943-110">Parte</span><span class="sxs-lookup"><span data-stu-id="eb943-110">Part</span></span>      | <span data-ttu-id="eb943-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb943-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb943-112">*Nome*</span><span class="sxs-lookup"><span data-stu-id="eb943-112">*Name*</span></span>    | <span data-ttu-id="eb943-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="eb943-113">Required.</span></span> <span data-ttu-id="eb943-114">Um valor de cadeia de caracteres correspondente à ID que você atribui ao [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="eb943-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="eb943-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="eb943-115">*RefName*</span></span> | <span data-ttu-id="eb943-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="eb943-116">Required.</span></span> <span data-ttu-id="eb943-117">Um valor de cadeia de caracteres correspondente ao nome (ID) do comando logo acima ou abaixo do local em que você deseja inserir o novo comando.</span><span class="sxs-lookup"><span data-stu-id="eb943-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="eb943-118">*Antes*</span><span class="sxs-lookup"><span data-stu-id="eb943-118">*Before*</span></span>  | <span data-ttu-id="eb943-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb943-119">Optional.</span></span> <span data-ttu-id="eb943-120">Um valor booliano que indica se o comando novo deve ser inserido antes do comando especificado por *refname*.</span><span class="sxs-lookup"><span data-stu-id="eb943-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="eb943-121">**True** (padrão).</span><span class="sxs-lookup"><span data-stu-id="eb943-121">**True** (Default).</span></span> <span data-ttu-id="eb943-122">O novo comando será inserido antes do comando referenciado.</span><span class="sxs-lookup"><span data-stu-id="eb943-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="eb943-123">**Falso** O novo comando será inserido após o comando referenciado.</span><span class="sxs-lookup"><span data-stu-id="eb943-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="eb943-124">*Legenda*</span><span class="sxs-lookup"><span data-stu-id="eb943-124">*Caption*</span></span> | <span data-ttu-id="eb943-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb943-125">Optional.</span></span> <span data-ttu-id="eb943-126">Um valor de cadeia de caracteres correspondente ao nome que aparecerá no menu pop-up do caractere e na janela de comandos quando o aplicativo cliente for de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="eb943-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="eb943-127">Para obter mais informações, consulte a propriedade [**Caption**](caption-property.md)do objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="eb943-128">*Voz*</span><span class="sxs-lookup"><span data-stu-id="eb943-128">*Voice*</span></span>   | <span data-ttu-id="eb943-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb943-129">Optional.</span></span> <span data-ttu-id="eb943-130">Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando.</span><span class="sxs-lookup"><span data-stu-id="eb943-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="eb943-131">Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a propriedade de **voz** do objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="eb943-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="eb943-132">*Enabled*</span></span> | <span data-ttu-id="eb943-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb943-133">Optional.</span></span> <span data-ttu-id="eb943-134">Um valor booliano que indica se o comando está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eb943-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="eb943-135">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="eb943-135">The default value is **True**.</span></span> <span data-ttu-id="eb943-136">Para obter mais informações, consulte a propriedade **Enabled** do objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="eb943-137">*Visível*</span><span class="sxs-lookup"><span data-stu-id="eb943-137">*Visible*</span></span> | <span data-ttu-id="eb943-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eb943-138">Optional.</span></span> <span data-ttu-id="eb943-139">Um valor booliano que indica se o comando está visível na janela de comandos quando o aplicativo cliente é de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="eb943-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="eb943-140">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="eb943-140">The default value is **True**.</span></span> <span data-ttu-id="eb943-141">Para obter mais informações, consulte a propriedade [**visível**](visible-property.md) do objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb943-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb943-142">Remarks</span></span>

<span data-ttu-id="eb943-143">O valor da propriedade [**Name**](name-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) deve ser exclusivo em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="eb943-144">Você deve remover um **comando** para poder criar um novo **comando** com a mesma configuração de propriedade de **nome** .</span><span class="sxs-lookup"><span data-stu-id="eb943-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="eb943-145">A tentativa de criar um **comando** com uma propriedade **Name** que já existe gera um erro.</span><span class="sxs-lookup"><span data-stu-id="eb943-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="eb943-146">Esse método também retorna um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="eb943-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="eb943-147">Isso permite que você declare um objeto e atribua um **comando** a ele ao chamar o método **Insert** .</span><span class="sxs-lookup"><span data-stu-id="eb943-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="eb943-148">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eb943-148">See Also</span></span>

<span data-ttu-id="eb943-149">Método [**Add**](add-method.md), método [**Remove**](remove-method.md), [**método RemoveAll**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="eb943-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

