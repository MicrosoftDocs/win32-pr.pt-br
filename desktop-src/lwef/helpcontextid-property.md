---
title: Propriedade HelpContextid (objeto de coleção de comandos)
description: Saiba mais sobre a propriedade HelpContextid do objeto da coleção de comandos. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068232"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="2975a-104">Propriedade HelpContextid (objeto de coleção de comandos)</span><span class="sxs-lookup"><span data-stu-id="2975a-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="2975a-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2975a-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2975a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="2975a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2975a-107">Retorna ou define um número de contexto associado para o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2975a-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="2975a-108">Usado para fornecer ajuda contextual para o objeto **Commands** .</span><span class="sxs-lookup"><span data-stu-id="2975a-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="2975a-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2975a-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2975a-110">\*Caracteres Agent. \***("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="2975a-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="2975a-111">Parte</span><span class="sxs-lookup"><span data-stu-id="2975a-111">Part</span></span>     | <span data-ttu-id="2975a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2975a-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="2975a-113">*Número*</span><span class="sxs-lookup"><span data-stu-id="2975a-113">*Number*</span></span> | <span data-ttu-id="2975a-114">Um inteiro que especifica um número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="2975a-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2975a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2975a-115">Remarks</span></span>

<span data-ttu-id="2975a-116">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionará o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2975a-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="2975a-117">Se você definir um número de contexto em **HelpContextId**, o Agent chamará ajuda e procurará o tópico identificado por esse número de contexto.</span><span class="sxs-lookup"><span data-stu-id="2975a-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="2975a-118">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="2975a-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="2975a-119">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2975a-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="2975a-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2975a-120">See Also</span></span>

[<span data-ttu-id="2975a-121">**Propriedade HelpFile**</span><span class="sxs-lookup"><span data-stu-id="2975a-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
