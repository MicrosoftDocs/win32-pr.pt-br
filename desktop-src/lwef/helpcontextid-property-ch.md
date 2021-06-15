---
title: Propriedade HelpContextID (objeto Characters)
description: Saiba mais sobre a propriedade HelpContextID do objeto Characters. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068178"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="18a92-104">Propriedade HelpContextID (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="18a92-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="18a92-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18a92-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="18a92-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18a92-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="18a92-107">Retorna ou define um número de contexto associado para o caractere.</span><span class="sxs-lookup"><span data-stu-id="18a92-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="18a92-108">Usado para fornecer Ajuda contextul para o caractere.</span><span class="sxs-lookup"><span data-stu-id="18a92-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="18a92-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="18a92-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="18a92-110">*agent.\***Characters("**_CharacterID_*_"). Número helpContextID_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="18a92-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="18a92-111">Parte</span><span class="sxs-lookup"><span data-stu-id="18a92-111">Part</span></span>     | <span data-ttu-id="18a92-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="18a92-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="18a92-113">*Número*</span><span class="sxs-lookup"><span data-stu-id="18a92-113">*Number*</span></span> | <span data-ttu-id="18a92-114">Um inteiro que especifica um número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="18a92-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18a92-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="18a92-115">Remarks</span></span>

<span data-ttu-id="18a92-116">Para dar suporte à Ajuda contextitivo para o caractere, atribua o número de contexto ao caractere que você usa para o tópico de Ajuda associado ao compilar o arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="18a92-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="18a92-117">Essa propriedade se aplica somente ao cliente do caractere; a configuração não afeta outros clientes do caractere ou outros caracteres do cliente.</span><span class="sxs-lookup"><span data-stu-id="18a92-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="18a92-118">Se você tiver criado um arquivo de Ajuda do Windows para seu aplicativo e definido a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário clicar no caractere.</span><span class="sxs-lookup"><span data-stu-id="18a92-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="18a92-119">Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="18a92-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="18a92-120">O número de contexto atual é o valor **de HelpContextID** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="18a92-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="18a92-121">A criação de um arquivo de Ajuda requer o Compilador da Ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18a92-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="18a92-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="18a92-122">See Also</span></span>

[<span data-ttu-id="18a92-123">**Propriedade HelpFile**</span><span class="sxs-lookup"><span data-stu-id="18a92-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




