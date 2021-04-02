---
title: Adicionar método
description: Adicionar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005406"
---
# <a name="add-method"></a><span data-ttu-id="38b24-103">Adicionar método</span><span class="sxs-lookup"><span data-stu-id="38b24-103">Add Method</span></span>

<span data-ttu-id="38b24-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38b24-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="38b24-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="38b24-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="38b24-106">Adiciona um objeto de [comando](the-command-object.md) à coleção de [comandos](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="38b24-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="38b24-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="38b24-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Comandos. Adicionar* \*  *nome*, *legenda*, *voz*, *habilitado*, *visível*</span><span class="sxs-lookup"><span data-stu-id="38b24-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="38b24-109">Parte</span><span class="sxs-lookup"><span data-stu-id="38b24-109">Part</span></span>      | <span data-ttu-id="38b24-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="38b24-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b24-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="38b24-111">*Name*</span></span>    | <span data-ttu-id="38b24-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="38b24-112">Required.</span></span> <span data-ttu-id="38b24-113">Um valor de cadeia de caracteres correspondente à ID que você atribui para o comando.</span><span class="sxs-lookup"><span data-stu-id="38b24-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="38b24-114">*Legenda*</span><span class="sxs-lookup"><span data-stu-id="38b24-114">*Caption*</span></span> | <span data-ttu-id="38b24-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38b24-115">Optional.</span></span> <span data-ttu-id="38b24-116">Um valor de cadeia de caracteres correspondente ao nome que aparecerá no menu pop-up do caractere e na janela de comandos quando o aplicativo cliente for de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="38b24-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="38b24-117">Para obter mais informações, consulte a propriedade [Caption](caption-property.md) do objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="38b24-118">*Voz*</span><span class="sxs-lookup"><span data-stu-id="38b24-118">*Voice*</span></span>   | <span data-ttu-id="38b24-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38b24-119">Optional.</span></span> <span data-ttu-id="38b24-120">Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando.</span><span class="sxs-lookup"><span data-stu-id="38b24-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="38b24-121">Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a propriedade de [voz](voice-property.md) do objeto de [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="38b24-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="38b24-122">*Enabled*</span></span> | <span data-ttu-id="38b24-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38b24-123">Optional.</span></span> <span data-ttu-id="38b24-124">Um valor booliano que indica se o comando está habilitado.</span><span class="sxs-lookup"><span data-stu-id="38b24-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="38b24-125">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="38b24-125">The default value is **True**.</span></span> <span data-ttu-id="38b24-126">Para obter mais informações, consulte a propriedade [Enabled](enabled-property.md) do objeto [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="38b24-127">*Visível*</span><span class="sxs-lookup"><span data-stu-id="38b24-127">*Visible*</span></span> | <span data-ttu-id="38b24-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="38b24-128">Optional.</span></span> <span data-ttu-id="38b24-129">Um valor booliano que indica se o comando está visível no menu pop-up do caractere para o caractere quando o aplicativo cliente é de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="38b24-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="38b24-130">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="38b24-130">The default value is **True**.</span></span> <span data-ttu-id="38b24-131">Para obter mais informações, consulte a propriedade [visível](visible-property.md) do objeto de [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b24-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="38b24-132">Remarks</span></span>

<span data-ttu-id="38b24-133">O valor da propriedade [Name](name-property.md) de um objeto de [comando](the-command-object.md) deve ser exclusivo em sua coleção de [comandos](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="38b24-134">Você deve remover um comando para poder criar um novo comando com a mesma configuração de propriedade de nome.</span><span class="sxs-lookup"><span data-stu-id="38b24-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="38b24-135">A tentativa de criar um comando com uma propriedade Name que já existe gera um erro.</span><span class="sxs-lookup"><span data-stu-id="38b24-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="38b24-136">Esse método também retorna um objeto de [comando](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="38b24-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="38b24-137">Isso permite que você declare um objeto e atribua um comando a ele ao chamar o addMethod.</span><span class="sxs-lookup"><span data-stu-id="38b24-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="38b24-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38b24-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b24-139">**Método insert**</span><span class="sxs-lookup"><span data-stu-id="38b24-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="38b24-140">**Método RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="38b24-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="38b24-141">**Remover método**</span><span class="sxs-lookup"><span data-stu-id="38b24-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




