---
title: Alterando a propriedade de plug-in do DSP de áudio de exemplo
description: Alterando a propriedade de plug-in do DSP de áudio de exemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, propriedades de áudio
- Plug-ins do DSP, propriedades de áudio
- plug-ins do DSP de áudio, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636463"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="86c52-108">Alterando a propriedade de plug-in do DSP de áudio de exemplo</span><span class="sxs-lookup"><span data-stu-id="86c52-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="86c52-109">Você provavelmente vai querer alterar a propriedade que o assistente de plug-in do Windows Media Player cria por padrão.</span><span class="sxs-lookup"><span data-stu-id="86c52-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="86c52-110">A lista a seguir detalha os itens que podem exigir alteração:</span><span class="sxs-lookup"><span data-stu-id="86c52-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="86c52-111">**O recurso de caixa de diálogo.**</span><span class="sxs-lookup"><span data-stu-id="86c52-111">**The dialog resource.**</span></span> <span data-ttu-id="86c52-112">Clique na guia **ResourceView** na janela espaço de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="86c52-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="86c52-113">Expanda a lista de pastas para abrir a pasta caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86c52-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="86c52-114">Clique duas vezes no recurso de caixa de diálogo para abrir o editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="86c52-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="86c52-115">Você pode fazer alterações na caixa de diálogo da página de propriedades para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="86c52-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="86c52-116">Por exemplo, você pode alterar o texto no rótulo ou substituir o controle de edição por uma caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="86c52-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="86c52-117">**O código do objeto da página de propriedades.**</span><span class="sxs-lookup"><span data-stu-id="86c52-117">**The property page object code.**</span></span> <span data-ttu-id="86c52-118">A implementação padrão usa uma variável do tipo Double para armazenar o fator de escala.</span><span class="sxs-lookup"><span data-stu-id="86c52-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="86c52-119">Você pode exigir um tipo diferente de dados.</span><span class="sxs-lookup"><span data-stu-id="86c52-119">You might require a different type of data.</span></span> <span data-ttu-id="86c52-120">Isso também exigiria que você alterasse o código que persiste os dados no registro e leia os dados do registro (incluindo o código que lê do registro em *CProjectName*::**FinalConstruct**).</span><span class="sxs-lookup"><span data-stu-id="86c52-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="86c52-121">**A variável de membro que armazena o valor da propriedade.**</span><span class="sxs-lookup"><span data-stu-id="86c52-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="86c52-122">Essa variável é denominada "m \_ fScaleFactor" e é declarada como tipo Double.</span><span class="sxs-lookup"><span data-stu-id="86c52-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="86c52-123">Talvez você queira alterar o nome e o tipo dessa variável em todo o projeto.</span><span class="sxs-lookup"><span data-stu-id="86c52-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="86c52-124">**Os métodos get e Property Put da propriedade.**</span><span class="sxs-lookup"><span data-stu-id="86c52-124">**The property get and property put methods.**</span></span> <span data-ttu-id="86c52-125">Talvez você queira alterar os nomes, os parâmetros e as implementações desses métodos.</span><span class="sxs-lookup"><span data-stu-id="86c52-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="86c52-126">Não se esqueça de também refletir essas alterações em outro lugar no projeto.</span><span class="sxs-lookup"><span data-stu-id="86c52-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="86c52-127">Por exemplo, o método de **aplicação** da página de propriedades chama **a \_ escala** *CProjectName*:: Put.</span><span class="sxs-lookup"><span data-stu-id="86c52-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86c52-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86c52-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86c52-129">**Implementando um plug-in do DSP de áudio**</span><span class="sxs-lookup"><span data-stu-id="86c52-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




