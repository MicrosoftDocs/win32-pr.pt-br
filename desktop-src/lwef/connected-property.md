---
title: Propriedade conectada
description: Propriedade conectada
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292461"
---
# <a name="connected-property"></a><span data-ttu-id="48db8-103">Propriedade conectada</span><span class="sxs-lookup"><span data-stu-id="48db8-103">Connected Property</span></span>

<span data-ttu-id="48db8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="48db8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="48db8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="48db8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="48db8-106">Retorna ou define se o controle atual está conectado ao servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="48db8-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="48db8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="48db8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="48db8-108">*Agent. \* \* \* conectado* \*  \[  =  *valor booleano*\]</span><span class="sxs-lookup"><span data-stu-id="48db8-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="48db8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="48db8-109">Part</span></span>      | <span data-ttu-id="48db8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="48db8-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48db8-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="48db8-111">*boolean*</span></span> | <span data-ttu-id="48db8-112">Uma expressão booliana que especifica se o controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="48db8-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="48db8-113">**Verdadeiro** O controle está conectado.</span><span class="sxs-lookup"><span data-stu-id="48db8-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48db8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48db8-114">Remarks</span></span>

<span data-ttu-id="48db8-115">Em muitas situações, especificar o controle cria automaticamente uma conexão com o servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="48db8-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="48db8-116">Por exemplo, especificar o CLSID do controle do Microsoft Agent na <OBJECT> marca em uma página da Web abre automaticamente uma conexão de servidor e sair da página fecha a conexão.</span><span class="sxs-lookup"><span data-stu-id="48db8-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="48db8-117">Da mesma forma, para Visual Basic ou outras linguagens que permitem que você descarte um controle em um formulário, executar o programa abre automaticamente uma conexão e sair do programa fecha a conexão.</span><span class="sxs-lookup"><span data-stu-id="48db8-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="48db8-118">Se o servidor não estiver em execução no momento, ele será iniciado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="48db8-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="48db8-119">No entanto, se você quiser criar um controle de agente em tempo de execução, talvez também seja necessário abrir explicitamente uma nova conexão com o servidor usando a propriedade **Connected** .</span><span class="sxs-lookup"><span data-stu-id="48db8-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="48db8-120">Por exemplo, no Visual Basic você pode criar um objeto ActiveX em tempo de execução usando a instrução SET com a **nova** palavra-chave (ou função CreateObject).</span><span class="sxs-lookup"><span data-stu-id="48db8-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="48db8-121">Embora isso crie o objeto, ele não pode criar a conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="48db8-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="48db8-122">Você pode usar a propriedade **Connected** antes de qualquer código que chame a interface de programação do Microsoft Agent, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="48db8-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="48db8-123">Criar um controle usando essa técnica não expõe os eventos do controle do agente.</span><span class="sxs-lookup"><span data-stu-id="48db8-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="48db8-124">No Visual Basic 5,0 (e posterior), você pode acessar os eventos do controle, incluindo o controle nas referências do seu projeto, e usar a palavra-chave **WithEvents** em sua declaração de variável:</span><span class="sxs-lookup"><span data-stu-id="48db8-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="48db8-125">O uso de **WithEvents** para criar uma instância do controle Agent em tempo de execução abre automaticamente a conexão com o servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="48db8-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="48db8-126">Portanto, você não precisa incluir uma instrução **conectada** .</span><span class="sxs-lookup"><span data-stu-id="48db8-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="48db8-127">Você pode fechar a conexão com o servidor liberando todas as referências que você criou para os objetos do Agent, como IAgentCtlCharacterEx e IAgentCtlCommandEx.</span><span class="sxs-lookup"><span data-stu-id="48db8-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="48db8-128">Você também deve liberar sua referência ao próprio controle Agent.</span><span class="sxs-lookup"><span data-stu-id="48db8-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="48db8-129">No Visual Basic, você pode liberar uma referência a um objeto definindo sua variável como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="48db8-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="48db8-130">Se você tiver carregado caracteres, descarregue-os antes de liberar o objeto de caractere.</span><span class="sxs-lookup"><span data-stu-id="48db8-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="48db8-131">Não é possível fechar a conexão com o servidor, liberando referências em que o componente foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="48db8-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="48db8-132">Por exemplo, você não pode fechar a conexão com o servidor em páginas da Web em que você usa a <OBJECT> marca para declarar o controle ou em um aplicativo Visual Basic onde você solta o controle em um formulário.</span><span class="sxs-lookup"><span data-stu-id="48db8-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="48db8-133">Embora a liberação de todas as referências de agente reduza o conjunto de trabalho do agente, a conexão permanece até que você navegue para a próxima página ou saia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48db8-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





