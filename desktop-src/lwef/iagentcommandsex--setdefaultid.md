---
title: IAgentCommandsEx setpadrão
description: IAgentCommandsEx setpadrão
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365916"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="93727-103">IAgentCommandsEx:: setpadrão</span><span class="sxs-lookup"><span data-stu-id="93727-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="93727-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93727-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="93727-105">Define a ID do comando padrão em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="93727-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="93727-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="93727-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="93727-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="93727-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="93727-108">A ID do [**comando**](/windows/desktop/lwef/the-command-object) a ser definido como o padrão.</span><span class="sxs-lookup"><span data-stu-id="93727-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="93727-109">Essa propriedade define o objeto de [**comando**](/windows/desktop/lwef/the-command-object) padrão definido em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="93727-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="93727-110">O comando padrão é negrito no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="93727-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="93727-111">No entanto, a definição do comando padrão não altera realmente o tratamento de comandos nem os eventos de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="93727-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="93727-112">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="93727-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="93727-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="93727-113">See Also</span></span>

[<span data-ttu-id="93727-114">**IAgentCommandsEx:: getdefaultid**</span><span class="sxs-lookup"><span data-stu-id="93727-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 