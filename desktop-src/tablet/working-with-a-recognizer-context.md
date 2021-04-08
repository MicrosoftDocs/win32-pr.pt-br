---
description: O objeto divisória usa uma RecognizerContext para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabalhando com um contexto de reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010569"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="63d83-103">Trabalhando com um contexto de reconhecedor</span><span class="sxs-lookup"><span data-stu-id="63d83-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="63d83-104">O objeto [**divisória**](inkdivider-class.md) usa uma [**RecognizerContext**](inkrecognizercontext-class.md) para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="63d83-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="63d83-105">Você pode definir o contexto do reconhecedor usando a propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) do objeto [**divisória**](inkdivider-class.md) ou fornecendo o contexto do reconhecedor na chamada para o construtor [divisória](/previous-versions/ms839465(v=msdn.10)) (em código gerenciado).</span><span class="sxs-lookup"><span data-stu-id="63d83-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="63d83-106">Se um contexto de reconhecedor para um reconhecedor não manuscrito ou para um reconhecedor que não ofereça suporte à funcionalidade de entrada gratuita for atribuído à propriedade **RecognizerContext** , uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="63d83-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="63d83-107">Se os reconhecedores não estiverem instalados ou se um contexto de reconhecedor não for atribuído ao objeto [**divisória**](inkdivider-class.md) , o objeto **divisória** não usará um contexto de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="63d83-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="63d83-108">Nesse caso, o recurso de análise de layout executa a divisão de segmento e nenhum texto é associado ao objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="63d83-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="63d83-109">A propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) não pode ser alterada após a atribuição de traços ao objeto [**divisória**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="63d83-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="63d83-110">O objeto **divisória** usa os valores de propriedade padrão do objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="63d83-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="63d83-111">O objeto [**divisória**](inkdivider-class.md) aplica o contexto do reconhecedor a elementos manuscritos durante a análise de layout.</span><span class="sxs-lookup"><span data-stu-id="63d83-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="63d83-112">Todos os traços que você atribui diretamente ao contexto do reconhecedor são ignorados pelo objeto **divisória** .</span><span class="sxs-lookup"><span data-stu-id="63d83-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="63d83-113">Para obter mais informações sobre reconhecimento de texto, consulte [sobre o reconhecimento de manuscrito](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="63d83-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
