---
title: O objeto Command
description: O objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105785266"
---
# <a name="the-command-object"></a><span data-ttu-id="da5fc-103">O objeto Command</span><span class="sxs-lookup"><span data-stu-id="da5fc-103">The Command Object</span></span>

<span data-ttu-id="da5fc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da5fc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="da5fc-105">Um objeto de [**comando**](/windows/desktop/lwef/the-command-object) é um item em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="da5fc-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="da5fc-106">O servidor fornece ao usuário acesso aos objetos de **comando** quando o aplicativo cliente se torna ativo.</span><span class="sxs-lookup"><span data-stu-id="da5fc-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="da5fc-107">Propriedades do objeto de comando</span><span class="sxs-lookup"><span data-stu-id="da5fc-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="da5fc-108">Para acessar a propriedade de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) , você faz referência a ela em sua coleção usando sua propriedade [**Name**](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="da5fc-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="da5fc-109">No VBScript e Visual Basic você pode usar a propriedade **Name** diretamente:</span><span class="sxs-lookup"><span data-stu-id="da5fc-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="da5fc-110">Para linguagens de programação que não dão suporte a coleções, use o método de [**comando**](command-method.md) :</span><span class="sxs-lookup"><span data-stu-id="da5fc-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="da5fc-111">Você também pode fazer referência a um objeto de comando criando uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="da5fc-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="da5fc-112">Em Visual Basic, declare uma variável de objeto e use a instrução SET para criar a referência:</span><span class="sxs-lookup"><span data-stu-id="da5fc-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="da5fc-113">No Visual Basic 5,0, você também pode declarar o objeto como o tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e criar a referência.</span><span class="sxs-lookup"><span data-stu-id="da5fc-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="da5fc-114">Essa convenção habilita a ligação antecipada, o que resulta em um melhor desempenho:</span><span class="sxs-lookup"><span data-stu-id="da5fc-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="da5fc-115">No VBScript, você pode declarar uma referência como um tipo específico, mas ainda pode declarar a variável e defini-la para o [**comando**](/windows/desktop/lwef/the-command-object) na coleção:</span><span class="sxs-lookup"><span data-stu-id="da5fc-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="da5fc-116">Um comando pode aparecer no menu pop-up do caractere e na janela comandos ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="da5fc-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="da5fc-117">Para aparecer no menu pop-up, ele deve ter uma legenda e ter a propriedade [**Visible**](visible-property.md) definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="da5fc-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="da5fc-118">Além disso, sua propriedade **Visible** do objeto de coleção de comandos também deve ser definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="da5fc-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="da5fc-119">Para aparecer na janela comandos, um [**comando**](/windows/desktop/lwef/the-command-object) deve ter suas propriedades [**Caption**](caption-property.md) e [**Voice**](voice-property.md) definidas.</span><span class="sxs-lookup"><span data-stu-id="da5fc-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="da5fc-120">Observe que as entradas de menu pop-up de um caractere não são alteradas enquanto o menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="da5fc-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="da5fc-121">Se você adicionar ou remover comandos ou alterar suas propriedades enquanto o menu pop-up do caractere for exibido, o menu exibirá essas alterações sempre que o usuário o exibir.</span><span class="sxs-lookup"><span data-stu-id="da5fc-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="da5fc-122">No entanto, a janela comandos reflete dinamicamente todas as alterações feitas.</span><span class="sxs-lookup"><span data-stu-id="da5fc-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="da5fc-123">A tabela a seguir resume como as propriedades de um [**comando**](/windows/desktop/lwef/the-command-object) afetam sua apresentação:</span><span class="sxs-lookup"><span data-stu-id="da5fc-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="da5fc-124">Propriedade Caption</span><span class="sxs-lookup"><span data-stu-id="da5fc-124">Caption Property</span></span>

<span data-ttu-id="da5fc-125">Propriedade Voice-Caption</span><span class="sxs-lookup"><span data-stu-id="da5fc-125">Voice-Caption Property</span></span>

<span data-ttu-id="da5fc-126">Propriedade de voz</span><span class="sxs-lookup"><span data-stu-id="da5fc-126">Voice Property</span></span>

<span data-ttu-id="da5fc-127">Propriedade Visible</span><span class="sxs-lookup"><span data-stu-id="da5fc-127">Visible Property</span></span>

<span data-ttu-id="da5fc-128">Propriedade Enabled</span><span class="sxs-lookup"><span data-stu-id="da5fc-128">Enabled Property</span></span>

<span data-ttu-id="da5fc-129">Aparece no menu pop-up do caractere</span><span class="sxs-lookup"><span data-stu-id="da5fc-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="da5fc-130">Aparece na janela de comandos</span><span class="sxs-lookup"><span data-stu-id="da5fc-130">Appears in Commands Window</span></span>

<span data-ttu-id="da5fc-131">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-131">Yes</span></span>

<span data-ttu-id="da5fc-132">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-132">Yes</span></span>

<span data-ttu-id="da5fc-133">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-133">Yes</span></span>

<span data-ttu-id="da5fc-134">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-134">True</span></span>

<span data-ttu-id="da5fc-135">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-135">True</span></span>

<span data-ttu-id="da5fc-136">Normal, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-137">Sim, usando [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="da5fc-138">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-138">Yes</span></span>

<span data-ttu-id="da5fc-139">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-139">Yes</span></span>

<span data-ttu-id="da5fc-140">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-140">Yes</span></span>

<span data-ttu-id="da5fc-141">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-141">True</span></span>

<span data-ttu-id="da5fc-142">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-142">False</span></span>

<span data-ttu-id="da5fc-143">Desabilitado, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-144">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-144">No</span></span>

<span data-ttu-id="da5fc-145">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-145">Yes</span></span>

<span data-ttu-id="da5fc-146">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-146">Yes</span></span>

<span data-ttu-id="da5fc-147">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-147">Yes</span></span>

<span data-ttu-id="da5fc-148">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-148">False</span></span>

<span data-ttu-id="da5fc-149">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-149">True</span></span>

<span data-ttu-id="da5fc-150">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-150">Does not appear</span></span>

<span data-ttu-id="da5fc-151">Sim, usando [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="da5fc-152">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-152">Yes</span></span>

<span data-ttu-id="da5fc-153">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-153">Yes</span></span>

<span data-ttu-id="da5fc-154">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-154">Yes</span></span>

<span data-ttu-id="da5fc-155">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-155">False</span></span>

<span data-ttu-id="da5fc-156">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-156">False</span></span>

<span data-ttu-id="da5fc-157">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-157">Does not appear</span></span>

<span data-ttu-id="da5fc-158">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-158">No</span></span>

<span data-ttu-id="da5fc-159">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-159">Yes</span></span>

<span data-ttu-id="da5fc-160">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-160">Yes</span></span>

<span data-ttu-id="da5fc-161">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-161">No</span></span> 

<span data-ttu-id="da5fc-162">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-162">True</span></span>

<span data-ttu-id="da5fc-163">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-163">True</span></span>

<span data-ttu-id="da5fc-164">Normal, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-165">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-165">No</span></span>

<span data-ttu-id="da5fc-166">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-166">Yes</span></span>

<span data-ttu-id="da5fc-167">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-167">Yes</span></span>

<span data-ttu-id="da5fc-168">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-168">No</span></span> 

<span data-ttu-id="da5fc-169">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-169">True</span></span>

<span data-ttu-id="da5fc-170">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-170">False</span></span>

<span data-ttu-id="da5fc-171">Desabilitado, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-172">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-172">No</span></span>

<span data-ttu-id="da5fc-173">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-173">Yes</span></span>

<span data-ttu-id="da5fc-174">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-174">Yes</span></span>

<span data-ttu-id="da5fc-175">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-175">No</span></span> 

<span data-ttu-id="da5fc-176">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-176">False</span></span>

<span data-ttu-id="da5fc-177">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-177">True</span></span>

<span data-ttu-id="da5fc-178">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-178">Does not appear</span></span>

<span data-ttu-id="da5fc-179">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-179">No</span></span>

<span data-ttu-id="da5fc-180">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-180">Yes</span></span>

<span data-ttu-id="da5fc-181">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-181">Yes</span></span>

<span data-ttu-id="da5fc-182">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-182">No</span></span> 

<span data-ttu-id="da5fc-183">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-183">False</span></span>

<span data-ttu-id="da5fc-184">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-184">False</span></span>

<span data-ttu-id="da5fc-185">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-185">Does not appear</span></span>

<span data-ttu-id="da5fc-186">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-186">No</span></span>

<span data-ttu-id="da5fc-187">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-187">No</span></span> 

<span data-ttu-id="da5fc-188">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-188">Yes</span></span>

<span data-ttu-id="da5fc-189">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-189">Yes</span></span>

<span data-ttu-id="da5fc-190">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-190">True</span></span>

<span data-ttu-id="da5fc-191">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-191">True</span></span>

<span data-ttu-id="da5fc-192">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-192">Does not appear</span></span>

<span data-ttu-id="da5fc-193">Sim, usando [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="da5fc-194">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-194">No</span></span> 

<span data-ttu-id="da5fc-195">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-195">Yes</span></span>

<span data-ttu-id="da5fc-196">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-196">Yes</span></span>

<span data-ttu-id="da5fc-197">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-197">True</span></span>

<span data-ttu-id="da5fc-198">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-198">False</span></span>

<span data-ttu-id="da5fc-199">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-199">Does not appear</span></span>

<span data-ttu-id="da5fc-200">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-200">No</span></span>

<span data-ttu-id="da5fc-201">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-201">No</span></span> 

<span data-ttu-id="da5fc-202">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-202">Yes</span></span>

<span data-ttu-id="da5fc-203">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-203">Yes</span></span>

<span data-ttu-id="da5fc-204">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-204">False</span></span>

<span data-ttu-id="da5fc-205">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-205">True</span></span>

<span data-ttu-id="da5fc-206">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-206">Does not appear</span></span>

<span data-ttu-id="da5fc-207">Sim, usando [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="da5fc-208">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-208">No</span></span> 

<span data-ttu-id="da5fc-209">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-209">Yes</span></span>

<span data-ttu-id="da5fc-210">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-210">Yes</span></span>

<span data-ttu-id="da5fc-211">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-211">False</span></span>

<span data-ttu-id="da5fc-212">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-212">False</span></span>

<span data-ttu-id="da5fc-213">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-213">Does not appear</span></span>

<span data-ttu-id="da5fc-214">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-214">No</span></span>

<span data-ttu-id="da5fc-215">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-215">No</span></span> 

<span data-ttu-id="da5fc-216">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-216">Yes</span></span>

<span data-ttu-id="da5fc-217">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-217">No</span></span> 

<span data-ttu-id="da5fc-218">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-218">True</span></span>

<span data-ttu-id="da5fc-219">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-219">True</span></span>

<span data-ttu-id="da5fc-220">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-220">Does not appear</span></span>

<span data-ttu-id="da5fc-221">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-221">No</span></span>

<span data-ttu-id="da5fc-222">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-222">No</span></span> 

<span data-ttu-id="da5fc-223">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-223">Yes</span></span>

<span data-ttu-id="da5fc-224">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-224">No</span></span> 

<span data-ttu-id="da5fc-225">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-225">True</span></span>

<span data-ttu-id="da5fc-226">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-226">False</span></span>

<span data-ttu-id="da5fc-227">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-227">Does not appear</span></span>

<span data-ttu-id="da5fc-228">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-228">No</span></span>

<span data-ttu-id="da5fc-229">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-229">No</span></span> 

<span data-ttu-id="da5fc-230">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-230">Yes</span></span>

<span data-ttu-id="da5fc-231">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-231">No</span></span> 

<span data-ttu-id="da5fc-232">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-232">False</span></span>

<span data-ttu-id="da5fc-233">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-233">True</span></span>

<span data-ttu-id="da5fc-234">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-234">Does not appear</span></span>

<span data-ttu-id="da5fc-235">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-235">No</span></span>

<span data-ttu-id="da5fc-236">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-236">No</span></span> 

<span data-ttu-id="da5fc-237">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-237">Yes</span></span>

<span data-ttu-id="da5fc-238">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-238">No</span></span> 

<span data-ttu-id="da5fc-239">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-239">False</span></span>

<span data-ttu-id="da5fc-240">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-240">False</span></span>

<span data-ttu-id="da5fc-241">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-241">Does not appear</span></span>

<span data-ttu-id="da5fc-242">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-242">No</span></span>

<span data-ttu-id="da5fc-243">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-243">Yes</span></span>

<span data-ttu-id="da5fc-244">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-244">No</span></span> 

<span data-ttu-id="da5fc-245">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-245">Yes</span></span>

<span data-ttu-id="da5fc-246">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-246">True</span></span>

<span data-ttu-id="da5fc-247">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-247">True</span></span>

<span data-ttu-id="da5fc-248">Normal, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-249">Sim, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-250">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-250">Yes</span></span>

<span data-ttu-id="da5fc-251">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-251">No</span></span> 

<span data-ttu-id="da5fc-252">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-252">Yes</span></span>

<span data-ttu-id="da5fc-253">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-253">True</span></span>

<span data-ttu-id="da5fc-254">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-254">False</span></span>

<span data-ttu-id="da5fc-255">Desabilitado, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-256">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-256">No</span></span>

<span data-ttu-id="da5fc-257">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-257">Yes</span></span>

<span data-ttu-id="da5fc-258">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-258">No</span></span> 

<span data-ttu-id="da5fc-259">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-259">Yes</span></span>

<span data-ttu-id="da5fc-260">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-260">False</span></span>

<span data-ttu-id="da5fc-261">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-261">True</span></span>

<span data-ttu-id="da5fc-262">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-262">Does not appear</span></span>

<span data-ttu-id="da5fc-263">Sim, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-264">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-264">Yes</span></span>

<span data-ttu-id="da5fc-265">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-265">No</span></span> 

<span data-ttu-id="da5fc-266">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-266">Yes</span></span>

<span data-ttu-id="da5fc-267">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-267">False</span></span>

<span data-ttu-id="da5fc-268">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-268">False</span></span>

<span data-ttu-id="da5fc-269">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-269">Does not appear</span></span>

<span data-ttu-id="da5fc-270">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-270">No</span></span>

<span data-ttu-id="da5fc-271">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-271">Yes</span></span>

<span data-ttu-id="da5fc-272">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-272">No</span></span> 

<span data-ttu-id="da5fc-273">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-273">No</span></span> 

<span data-ttu-id="da5fc-274">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-274">True</span></span>

<span data-ttu-id="da5fc-275">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-275">True</span></span>

<span data-ttu-id="da5fc-276">Normal, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-277">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-277">No</span></span>

<span data-ttu-id="da5fc-278">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-278">Yes</span></span>

<span data-ttu-id="da5fc-279">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-279">No</span></span> 

<span data-ttu-id="da5fc-280">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-280">No</span></span> 

<span data-ttu-id="da5fc-281">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-281">True</span></span>

<span data-ttu-id="da5fc-282">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-282">False</span></span>

<span data-ttu-id="da5fc-283">Desabilitado, usando [ **legenda**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="da5fc-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="da5fc-284">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-284">No</span></span>

<span data-ttu-id="da5fc-285">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-285">Yes</span></span>

<span data-ttu-id="da5fc-286">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-286">No</span></span> 

<span data-ttu-id="da5fc-287">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-287">No</span></span> 

<span data-ttu-id="da5fc-288">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-288">False</span></span>

<span data-ttu-id="da5fc-289">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-289">True</span></span>

<span data-ttu-id="da5fc-290">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-290">Does not appear</span></span>

<span data-ttu-id="da5fc-291">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-291">No</span></span>

<span data-ttu-id="da5fc-292">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-292">Yes</span></span>

<span data-ttu-id="da5fc-293">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-293">No</span></span> 

<span data-ttu-id="da5fc-294">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-294">No</span></span> 

<span data-ttu-id="da5fc-295">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-295">False</span></span>

<span data-ttu-id="da5fc-296">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-296">False</span></span>

<span data-ttu-id="da5fc-297">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-297">Does not appear</span></span>

<span data-ttu-id="da5fc-298">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-298">No</span></span>

<span data-ttu-id="da5fc-299">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-299">No</span></span> 

<span data-ttu-id="da5fc-300">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-300">No</span></span> 

<span data-ttu-id="da5fc-301">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-301">Yes</span></span>

<span data-ttu-id="da5fc-302">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-302">True</span></span>

<span data-ttu-id="da5fc-303">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-303">True</span></span>

<span data-ttu-id="da5fc-304">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-304">Does not appear</span></span>

<span data-ttu-id="da5fc-305">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-305">No</span></span> 

<span data-ttu-id="da5fc-306">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-306">No</span></span> 

<span data-ttu-id="da5fc-307">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-307">No</span></span> 

<span data-ttu-id="da5fc-308">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-308">Yes</span></span>

<span data-ttu-id="da5fc-309">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-309">True</span></span>

<span data-ttu-id="da5fc-310">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-310">False</span></span>

<span data-ttu-id="da5fc-311">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-311">Does not appear</span></span>

<span data-ttu-id="da5fc-312">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-312">No</span></span>

<span data-ttu-id="da5fc-313">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-313">No</span></span> 

<span data-ttu-id="da5fc-314">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-314">No</span></span> 

<span data-ttu-id="da5fc-315">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-315">Yes</span></span>

<span data-ttu-id="da5fc-316">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-316">False</span></span>

<span data-ttu-id="da5fc-317">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-317">True</span></span>

<span data-ttu-id="da5fc-318">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-318">Does not appear</span></span>

<span data-ttu-id="da5fc-319">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-319">No</span></span> 

<span data-ttu-id="da5fc-320">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-320">No</span></span> 

<span data-ttu-id="da5fc-321">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-321">No</span></span> 

<span data-ttu-id="da5fc-322">Sim</span><span class="sxs-lookup"><span data-stu-id="da5fc-322">Yes</span></span>

<span data-ttu-id="da5fc-323">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-323">False</span></span>

<span data-ttu-id="da5fc-324">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-324">False</span></span>

<span data-ttu-id="da5fc-325">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-325">Does not appear</span></span>

<span data-ttu-id="da5fc-326">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-326">No</span></span>

<span data-ttu-id="da5fc-327">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-327">No</span></span> 

<span data-ttu-id="da5fc-328">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-328">No</span></span> 

<span data-ttu-id="da5fc-329">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-329">No</span></span> 

<span data-ttu-id="da5fc-330">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-330">True</span></span>

<span data-ttu-id="da5fc-331">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-331">True</span></span>

<span data-ttu-id="da5fc-332">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-332">Does not appear</span></span>

<span data-ttu-id="da5fc-333">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-333">No</span></span>

<span data-ttu-id="da5fc-334">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-334">No</span></span> 

<span data-ttu-id="da5fc-335">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-335">No</span></span> 

<span data-ttu-id="da5fc-336">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-336">No</span></span> 

<span data-ttu-id="da5fc-337">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-337">True</span></span>

<span data-ttu-id="da5fc-338">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-338">False</span></span>

<span data-ttu-id="da5fc-339">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-339">Does not appear</span></span>

<span data-ttu-id="da5fc-340">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-340">No</span></span>

<span data-ttu-id="da5fc-341">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-341">No</span></span> 

<span data-ttu-id="da5fc-342">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-342">No</span></span> 

<span data-ttu-id="da5fc-343">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-343">No</span></span> 

<span data-ttu-id="da5fc-344">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-344">False</span></span>

<span data-ttu-id="da5fc-345">True</span><span class="sxs-lookup"><span data-stu-id="da5fc-345">True</span></span>

<span data-ttu-id="da5fc-346">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-346">Does not appear</span></span>

<span data-ttu-id="da5fc-347">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-347">No</span></span>

<span data-ttu-id="da5fc-348">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-348">No</span></span> 

<span data-ttu-id="da5fc-349">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-349">No</span></span> 

<span data-ttu-id="da5fc-350">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-350">No</span></span> 

<span data-ttu-id="da5fc-351">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-351">False</span></span>

<span data-ttu-id="da5fc-352">Falso</span><span class="sxs-lookup"><span data-stu-id="da5fc-352">False</span></span>

<span data-ttu-id="da5fc-353">Não aparece</span><span class="sxs-lookup"><span data-stu-id="da5fc-353">Does not appear</span></span>

<span data-ttu-id="da5fc-354">Não</span><span class="sxs-lookup"><span data-stu-id="da5fc-354">No</span></span>

 <span data-ttu-id="da5fc-355">Se a configuração da propriedade for nula.</span><span class="sxs-lookup"><span data-stu-id="da5fc-355">If the property setting is null.</span></span> <span data-ttu-id="da5fc-356">Em algumas linguagens de programação, uma cadeia de caracteres vazia não pode ser interpretada da mesma forma que uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="da5fc-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="da5fc-357">O comando ainda é acessível por voz.</span><span class="sxs-lookup"><span data-stu-id="da5fc-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="da5fc-358">Quando o servidor recebe entrada para um de seus comandos, ele envia um evento de [**comando**](/windows/desktop/lwef/the-command-object) e retorna o nome do **comando** como um atributo do objeto [**userinput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="da5fc-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="da5fc-359">Em seguida, você pode usar instruções condicionais para fazer a correspondência e processar o **comando**.</span><span class="sxs-lookup"><span data-stu-id="da5fc-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

