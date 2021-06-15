---
title: Propriedade HelpContextid (objeto Command)
description: Saiba mais sobre a propriedade HelpContextid do objeto Command. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068503"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="15d6f-104">Propriedade HelpContextid (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="15d6f-104">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="15d6f-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15d6f-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="15d6f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="15d6f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="15d6f-107">Retorna ou define um número de contexto associado para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="15d6f-107">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="15d6f-108">Usado para fornecer ajuda contextual para o objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="15d6f-108">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="15d6f-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="15d6f-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="15d6f-110">\*Caracteres Agent. \***("**_characterid_\*_"). Comandos ("")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="15d6f-110">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="15d6f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="15d6f-111">Part</span></span>     | <span data-ttu-id="15d6f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="15d6f-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="15d6f-113">*Número*</span><span class="sxs-lookup"><span data-stu-id="15d6f-113">*Number*</span></span> | <span data-ttu-id="15d6f-114">Um inteiro que especifica um número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="15d6f-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15d6f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="15d6f-115">Remarks</span></span>

<span data-ttu-id="15d6f-116">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere como o arquivo, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) for definido como **true** e o usuário selecionar o comando.</span><span class="sxs-lookup"><span data-stu-id="15d6f-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="15d6f-117">Se você definir um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="15d6f-117">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="15d6f-118">O número de contexto atual é o valor de **HelpContextId** para o comando.</span><span class="sxs-lookup"><span data-stu-id="15d6f-118">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="15d6f-119">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="15d6f-119">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="15d6f-120">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="15d6f-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="15d6f-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="15d6f-121">See Also</span></span>

[<span data-ttu-id="15d6f-122">**Propriedade HelpFile**</span><span class="sxs-lookup"><span data-stu-id="15d6f-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 
