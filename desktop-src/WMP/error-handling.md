---
title: Tratamento de erro (SDK do Windows Media Player)
description: Tratamento de erros
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, tratamento de erros
- Modelo de objeto do Windows Media Player, tratamento de erros
- modelo de objeto, tratamento de erro
- Controle ActiveX do Windows Media Player, tratamento de erros
- Controle ActiveX, tratamento de erros
- Controle ActiveX móvel do Windows Media Player, tratamento de erros
- Windows Media Player Mobile, tratamento de erros
- Guia de migração, tratamento de erros
- tratamento de erro no modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085036"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="2d2e7-112">Tratamento de erro (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="2d2e7-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="2d2e7-113">O controle ActiveX do Windows Media Player 6,4 Fornece tratamento de erros padrão exibindo mensagens de erro em caixas de diálogo e na barra de status.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="2d2e7-114">Você também pode fornecer tratamento de erros personalizado processando erros em seu script.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="2d2e7-115">O tratamento de erros é controlado por eventos, o que significa que você recebe uma notificação para cada erro e deve decidir como lidar com cada evento de erro quando ele ocorre.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="2d2e7-116">Para obter mais informações sobre como tratar erros usando o modelo de objeto da versão 6,4, consulte a seção tratamento de erros do guia do modelo de objeto da versão 6,4 do Player, que faz parte do SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="2d2e7-117">O modelo de objeto do Windows Media Player 7 ou posterior fornece o objeto **Error** e o objeto **ErrorItem** para lidar com erros.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="2d2e7-118">Esses dois objetos funcionam em conjunto para fornecer a você um mecanismo de tratamento de erros que oferece controle completo e flexível do processo de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="2d2e7-119">O objeto **Error** fornece acesso a uma coleção de objetos **ErrorItem** ; cada objeto **ErrorItem** fornece detalhes sobre uma mensagem de erro individual.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="2d2e7-120">Quando ocorre um erro, as informações de erro são postadas em uma fila de erros.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="2d2e7-121">A fila é uma coleção de objetos **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="2d2e7-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="2d2e7-122">À medida que cada erro é adicionado à fila, ele é associado a um número de índice (começando com zero) que pode ser usado para identificar o objeto **ErrorItem** específico.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="2d2e7-123">O *erro*. a propriedade **errorCount** recupera o número de erros na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="2d2e7-124">Como os números de índice são baseados em zero, o erro mais recente Postado na fila sempre terá um valor de índice igual a *erro*. **errorCount** menos um.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="2d2e7-125">Você pode criar um manipulador de eventos de erro para o Windows Media Player usando o script.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="2d2e7-126">O exemplo de JScript a seguir mostra como recuperar o item de erro mais recente da fila de erros e exibir o código de erro e a descrição do erro usando o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="2d2e7-127">O objeto de **jogador** foi criado com ID = "WMP9".</span><span class="sxs-lookup"><span data-stu-id="2d2e7-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="2d2e7-128">O objeto de **erro** tem dois métodos adicionais que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="2d2e7-129">O *erro*. o método **clearErrorQueue** permite remover todos os erros da fila de erros e redefinir o número de índice para zero.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="2d2e7-130">Você tem controle total sobre esse processo; Você pode manter os erros na fila pelo tempo que precisar que estejam disponíveis e, em seguida, esvaziar a fila quando terminar de lidar com os erros.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="2d2e7-131">O *erro*. o método **WebHelp** fornece uma maneira de exibir as informações de erro mais recentes para o usuário usando a Internet.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="2d2e7-132">Quando chamado, esse método transfere todas as informações relevantes sobre o primeiro erro na fila (aquela com índice zero) para a ajuda da Web do Microsoft Windows Media Player, que exibe informações adicionais sobre o erro na janela atual do navegador.</span><span class="sxs-lookup"><span data-stu-id="2d2e7-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d2e7-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d2e7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d2e7-134">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="2d2e7-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="2d2e7-135">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="2d2e7-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="2d2e7-136">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="2d2e7-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




