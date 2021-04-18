---
title: Propriedade HelpContextid (objeto characters)
description: Propriedade HelpContextid
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369100"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="de08b-103">Propriedade HelpContextid (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="de08b-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="de08b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de08b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="de08b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="de08b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="de08b-106">Retorna ou define um número de contexto associado para o caractere.</span><span class="sxs-lookup"><span data-stu-id="de08b-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="de08b-107">Usado para fornecer ajuda contextual para o caractere.</span><span class="sxs-lookup"><span data-stu-id="de08b-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="de08b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="de08b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="de08b-109">\*Caracteres Agent. \***("**_characterid_\*_")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="de08b-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="de08b-110">Parte</span><span class="sxs-lookup"><span data-stu-id="de08b-110">Part</span></span>     | <span data-ttu-id="de08b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="de08b-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="de08b-112">*Número*</span><span class="sxs-lookup"><span data-stu-id="de08b-112">*Number*</span></span> | <span data-ttu-id="de08b-113">Um inteiro que especifica um número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="de08b-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de08b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="de08b-114">Remarks</span></span>

<span data-ttu-id="de08b-115">Para dar suporte à ajuda contextual para o caractere, atribua o número de contexto ao caractere que você usa para o tópico da ajuda associado ao compilar o arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="de08b-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="de08b-116">Essa propriedade aplica-se somente ao cliente do caractere; a configuração não afeta outros clientes do caractere ou outros caracteres do cliente.</span><span class="sxs-lookup"><span data-stu-id="de08b-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="de08b-117">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) for definido como **true** e o usuário clicar no caractere.</span><span class="sxs-lookup"><span data-stu-id="de08b-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="de08b-118">Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual.</span><span class="sxs-lookup"><span data-stu-id="de08b-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="de08b-119">O número de contexto atual é o valor de **HelpContextId** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="de08b-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="de08b-120">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="de08b-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="de08b-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="de08b-121">See Also</span></span>

[<span data-ttu-id="de08b-122">**Propriedade HelpFile**</span><span class="sxs-lookup"><span data-stu-id="de08b-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




