---
title: IAgentCharacterEx getarquivodeajudaname
description: IAgentCharacterEx getarquivodeajudaname
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916473"
---
# <a name="iagentcharacterexgethelpfilename"></a><span data-ttu-id="7968d-103">IAgentCharacterEx:: getarquivodeajudaname</span><span class="sxs-lookup"><span data-stu-id="7968d-103">IAgentCharacterEx::GetHelpFileName</span></span>

<span data-ttu-id="7968d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7968d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

<span data-ttu-id="7968d-105">Recupera o HelpFilename de um caractere.</span><span class="sxs-lookup"><span data-stu-id="7968d-105">Retrieves the HelpFileName for a character.</span></span>

-   <span data-ttu-id="7968d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7968d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7968d-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="7968d-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="7968d-108">Endereço de uma variável que recebe o nome de arquivo da ajuda para o caractere.</span><span class="sxs-lookup"><span data-stu-id="7968d-108">Address of a variable that receives the Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="7968d-109">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário clicar no caractere ou selecionar um comando no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="7968d-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="7968d-110">Se houver um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".</span><span class="sxs-lookup"><span data-stu-id="7968d-110">If there is a context number in the selected command's [**HelpContextID**](helpcontextid-property.md) property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="7968d-111">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="7968d-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="7968d-112">A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7968d-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7968d-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7968d-113">See Also</span></span>

<span data-ttu-id="7968d-114">[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="7968d-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




