---
title: Por que usar a estrutura de serviços de texto
description: Por que usar a estrutura de serviços de texto
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- TSF (estrutura de serviços de texto), sobre
- TSF (estrutura de serviços de texto), sobre
- serviços de texto, sobre
- Aplicativos habilitados para TSF, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105767776"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="9380e-107">Por que usar a estrutura de serviços de texto?</span><span class="sxs-lookup"><span data-stu-id="9380e-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="9380e-108">A TSF (estrutura de serviços de texto) permite que um aplicativo habilitado para TSF receba entrada de texto de qualquer número de dispositivos ou fontes.</span><span class="sxs-lookup"><span data-stu-id="9380e-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="9380e-109">Como o TSF é extensível, o aplicativo pode receber entrada de texto de fontes de texto adicionais com pouca ou nenhuma modificação.</span><span class="sxs-lookup"><span data-stu-id="9380e-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="9380e-110">Um serviço de texto Obtém texto de e fornece texto para qualquer aplicativo habilitado para TSF sem a necessidade de qualquer conhecimento sobre o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9380e-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="9380e-111">Essa estrutura permite que o serviço de texto esteja disponível para qualquer aplicativo habilitado para TSF.</span><span class="sxs-lookup"><span data-stu-id="9380e-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="9380e-112">O serviço de texto pode ser instalado ou atualizado como um módulo separado e independente de qualquer aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="9380e-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="9380e-113">O TSF também permite que um serviço de texto armazene metadados com um documento, um pedaço de texto ou um objeto dentro do documento.</span><span class="sxs-lookup"><span data-stu-id="9380e-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="9380e-114">Por exemplo, um serviço de texto de entrada de fala pode armazenar informações de som associadas a um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="9380e-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="9380e-115">O TSF permite que os serviços de texto forneçam uma conversão de texto precisa e completa, com acesso contínuo ao buffer do documento.</span><span class="sxs-lookup"><span data-stu-id="9380e-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="9380e-116">Os serviços de texto usando o TSF podem evitar separar sua funcionalidade em modos de entrada e modos para edição.</span><span class="sxs-lookup"><span data-stu-id="9380e-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="9380e-117">Essa arquitetura de entrada permite que o fluxo de texto em buffer e acumulado seja alterado dinamicamente, permitindo uma entrada de teclado e edição de texto mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="9380e-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="9380e-118">O TSF é independente de dispositivo e permite serviços de texto para vários dispositivos de entrada, incluindo teclado, caneta e microfone.</span><span class="sxs-lookup"><span data-stu-id="9380e-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




