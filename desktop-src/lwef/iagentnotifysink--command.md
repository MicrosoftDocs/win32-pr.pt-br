---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917240"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="06a45-103">IAgentNotifySink:: comando</span><span class="sxs-lookup"><span data-stu-id="06a45-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="06a45-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="06a45-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="06a45-105">Notifica um aplicativo cliente de que um [**comando**](/windows/desktop/lwef/the-command-object) foi selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="06a45-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="06a45-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="06a45-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="06a45-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="06a45-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="06a45-108">Identificador da melhor alternativa de comando de correspondência.</span><span class="sxs-lookup"><span data-stu-id="06a45-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="06a45-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span><span class="sxs-lookup"><span data-stu-id="06a45-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="06a45-110">Endereço da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para o objeto [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="06a45-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="06a45-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar a interface [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="06a45-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="06a45-112">O servidor notifica o cliente de entrada-ativo quando o usuário escolhe um comando por voz ou selecionando um comando no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="06a45-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="06a45-113">O evento ocorre mesmo quando o usuário seleciona um dos comandos do servidor.</span><span class="sxs-lookup"><span data-stu-id="06a45-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="06a45-114">Nesse caso, o servidor retorna uma ID de comando nula, a pontuação de confiança e o texto de voz retornado pelo mecanismo de fala para essa entrada.</span><span class="sxs-lookup"><span data-stu-id="06a45-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="06a45-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="06a45-115">See Also</span></span>

[<span data-ttu-id="06a45-116">**IAgentUserInput**</span><span class="sxs-lookup"><span data-stu-id="06a45-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 