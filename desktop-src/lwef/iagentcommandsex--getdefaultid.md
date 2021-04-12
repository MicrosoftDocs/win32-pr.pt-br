---
title: IAgentCommandsEx getpadrão
description: IAgentCommandsEx getpadrão
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366013"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="b6cfb-103">IAgentCommandsEx:: getdefaultid</span><span class="sxs-lookup"><span data-stu-id="b6cfb-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="b6cfb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6cfb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="b6cfb-105">Recupera a ID do comando padrão em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b6cfb-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="b6cfb-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b6cfb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b6cfb-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="b6cfb-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="b6cfb-108">Endereço de uma variável que recebe a ID do conjunto de [**comandos**](/windows/desktop/lwef/the-command-object) como padrão.</span><span class="sxs-lookup"><span data-stu-id="b6cfb-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="b6cfb-109">Essa propriedade retorna o objeto de [**comando**](/windows/desktop/lwef/the-command-object) padrão atual em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b6cfb-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="b6cfb-110">O comando padrão é negrito no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="b6cfb-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="b6cfb-111">No entanto, a definição do comando padrão não altera o tratamento de comandos nem eventos de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="b6cfb-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="b6cfb-112">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b6cfb-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6cfb-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b6cfb-113">See Also</span></span>

[<span data-ttu-id="b6cfb-114">**IAgentCommandsEx:: setpadrão**</span><span class="sxs-lookup"><span data-stu-id="b6cfb-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 