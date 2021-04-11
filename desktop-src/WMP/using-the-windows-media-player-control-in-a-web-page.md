---
title: Usando o controle do Windows Media Player em uma página da Web
description: Usando o controle do Windows Media Player em uma página da Web
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- inserindo, páginas da Web
- Inserção de página da Web, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160111"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="e288c-115">Usando o controle do Windows Media Player em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="e288c-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="e288c-116">A inserção do controle do Windows Media Player em uma página da Web permite que você personalize completamente a maneira como o usuário interage com o controle.</span><span class="sxs-lookup"><span data-stu-id="e288c-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="e288c-117">Você pode usar a interface fornecida pelo controle ou pode ocultá-la e exibir sua própria interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e288c-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="e288c-118">Você pode especificar várias propriedades de controle do Windows Media Player no ponto em que você insere o controle ou pode definir as propriedades do Player e chamar os métodos do Player no código do script.</span><span class="sxs-lookup"><span data-stu-id="e288c-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="e288c-119">As seções a seguir descrevem as noções básicas de inserção do controle em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="e288c-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="e288c-120">Seção</span><span class="sxs-lookup"><span data-stu-id="e288c-120">Section</span></span>                                                                                                        | <span data-ttu-id="e288c-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e288c-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e288c-122">Ocultando o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e288c-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="e288c-123">Descreve as opções para ocultar o controle do Windows Media Player quando você deseja fornecer sua própria interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e288c-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="e288c-124">Elementos PARAM em um elemento OBJECT</span><span class="sxs-lookup"><span data-stu-id="e288c-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="e288c-125">Descreve como inicializar o controle do Windows Media Player ao incorporá-lo.</span><span class="sxs-lookup"><span data-stu-id="e288c-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="e288c-126">Exemplo simples de script em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="e288c-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="e288c-127">Descreve um exemplo simples, mas completo, de um controle de player incorporado com uma interface de usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="e288c-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="e288c-128">Usando o controle do Windows Media Player com o Firefox</span><span class="sxs-lookup"><span data-stu-id="e288c-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="e288c-129">Descreve como inserir o controle do Windows Media Player em uma página da Web para que ele seja exibido corretamente por um navegador Firefox.</span><span class="sxs-lookup"><span data-stu-id="e288c-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="e288c-130">Uso do Windows Media Player com o Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="e288c-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="e288c-131">Descreve como usar o controle do Windows Media Player com o Netscape 7,1 e outros navegadores da Web baseados em Gecko.</span><span class="sxs-lookup"><span data-stu-id="e288c-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="e288c-132">O controle móvel do Windows Media Player 10 contém funcionalidade baseada em um subconjunto da funcionalidade fornecida na versão da área de trabalho do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e288c-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="e288c-133">Portanto, ele pode ser inserido em uma página da Web do Pocket Internet Explorer da mesma maneira que o controle de área de trabalho é inserido em uma página da Web do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e288c-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="e288c-134">Para descobrir se um determinado método, propriedade ou evento tem suporte para o controle móvel do Windows Media Player 10, consulte [referência de modelo de objeto para scripts](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="e288c-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e288c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e288c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e288c-136">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="e288c-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




