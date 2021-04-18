---
title: Propriedade HelpContextid (objeto de coleção de comandos)
description: Propriedade HelpContextid
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454548"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="fa732-103">Propriedade HelpContextid (objeto de coleção de comandos)</span><span class="sxs-lookup"><span data-stu-id="fa732-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="fa732-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa732-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fa732-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="fa732-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fa732-106">Retorna ou define um número de contexto associado para o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fa732-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="fa732-107">Usado para fornecer ajuda contextual para o objeto **Commands** .</span><span class="sxs-lookup"><span data-stu-id="fa732-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="fa732-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="fa732-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fa732-109">\*Caracteres Agent. \***("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="fa732-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="fa732-110">Parte</span><span class="sxs-lookup"><span data-stu-id="fa732-110">Part</span></span>     | <span data-ttu-id="fa732-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa732-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="fa732-112">*Número*</span><span class="sxs-lookup"><span data-stu-id="fa732-112">*Number*</span></span> | <span data-ttu-id="fa732-113">Um inteiro que especifica um número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="fa732-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa732-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa732-114">Remarks</span></span>

<span data-ttu-id="fa732-115">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionará o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fa732-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="fa732-116">Se você definir um número de contexto em **HelpContextId**, o Agent chamará ajuda e procurará o tópico identificado por esse número de contexto.</span><span class="sxs-lookup"><span data-stu-id="fa732-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="fa732-117">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="fa732-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="fa732-118">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fa732-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="fa732-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fa732-119">See Also</span></span>

[<span data-ttu-id="fa732-120">**Propriedade HelpFile**</span><span class="sxs-lookup"><span data-stu-id="fa732-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
