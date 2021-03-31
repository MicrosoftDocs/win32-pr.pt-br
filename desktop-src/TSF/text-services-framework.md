---
title: Estrutura de serviços de texto (estrutura de serviços de texto)
description: O Microsoft Windows Text Services Framework (TSF) é um serviço de sistema disponível como um pacote redistribuível para o Windows 2000.
ms.assetid: ecc34b2e-89e8-48a8-8a8e-442d2145fe24
ms.topic: article
ms.date: 01/14/2020
ms.openlocfilehash: 9c21cae442b5fbed62c00010a17849d1d5f27b49
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644122"
---
# <a name="text-services-framework-text-services-framework"></a><span data-ttu-id="5eb3d-103">Estrutura de serviços de texto (estrutura de serviços de texto)</span><span class="sxs-lookup"><span data-stu-id="5eb3d-103">Text Services Framework (Text Services Framework)</span></span>

## <a name="purpose"></a><span data-ttu-id="5eb3d-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="5eb3d-104">Purpose</span></span>

<span data-ttu-id="5eb3d-105">O Microsoft Windows Text Services Framework (TSF) é um serviço de sistema disponível como um pacote redistribuível para o Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-105">Microsoft Windows Text Services Framework (TSF) is a system service available as a redistributable for Windows.</span></span> <span data-ttu-id="5eb3d-106">O TSF fornece uma estrutura simples e escalonável para a entrega de tecnologias avançadas de entrada de texto e linguagem natural.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-106">TSF provides a simple and scalable framework for the delivery of advanced text input and natural language technologies.</span></span> <span data-ttu-id="5eb3d-107">O TSF pode ser habilitado em aplicativos ou como um serviço de texto do TSF.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-107">TSF can be enabled in applications, or as a TSF text service.</span></span> <span data-ttu-id="5eb3d-108">Um serviço de texto do TSF fornece suporte multilíngue e fornece serviços de texto, como processadores de teclado, reconhecimento de manuscrito e reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-108">A TSF text service provides multilingual support and delivers text services such as keyboard processors, handwriting recognition, and speech recognition.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5eb3d-109">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="5eb3d-109">Where applicable</span></span>

<span data-ttu-id="5eb3d-110">A estrutura de serviços de texto é aplicável a computadores baseados no Windows usando serviços de texto e o Windows XP ou versões posteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-110">Text Services Framework is applicable for Windows-based computers using text services and Windows XP or later versions of the operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5eb3d-111">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="5eb3d-111">Developer audience</span></span>

<span data-ttu-id="5eb3d-112">A estrutura de serviços de texto é projetada para uso por programadores de Component Object Model (COM) usando as linguagens de programação C/C++.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-112">Text Services Framework is designed for use by Component Object Model (COM) programmers using the C/C++ programming languages.</span></span> <span data-ttu-id="5eb3d-113">Os programadores devem estar familiarizados com os serviços de texto para computadores baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-113">Programmers should be familiar with text services for Windows-based computers.</span></span> <span data-ttu-id="5eb3d-114">É recomendável conhecer o reconhecimento de manuscrito, o reconhecimento de fala e a programação de suporte multilíngüe.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-114">Knowledge of handwriting recognition, speech recognition, and programming for multilingual support is recommended.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5eb3d-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="5eb3d-115">Run-time requirements</span></span>

<span data-ttu-id="5eb3d-116">Para os pacotes redistribuíveis mais recentes, baixe o [SDK da plataforma Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="5eb3d-116">For the latest redistributable, download the [Windows 10 platform SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>

<span data-ttu-id="5eb3d-117">Para obter mais informações sobre os requisitos de elementos específicos da API, consulte a seção requisitos na documentação do] (/Windows/Win32/TSF/Text-Services-Framework-Reference) [referência do TFS.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-117">For more information about the requirements of specific API elements, see the Requirements section in the ](/windows/win32/tsf/text-services-framework-reference)[TFS reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eb3d-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5eb3d-118">In this section</span></span>



| <span data-ttu-id="5eb3d-119">Tópico</span><span class="sxs-lookup"><span data-stu-id="5eb3d-119">Topic</span></span>                                                                                 | <span data-ttu-id="5eb3d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eb3d-120">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb3d-121">Sobre a estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="5eb3d-121">About Text Services Framework</span></span>](about-text-services-framework.md)<br/>         | <span data-ttu-id="5eb3d-122">Informações gerais sobre a estrutura de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-122">General information about Text Services Framework.</span></span><br/>                                                    |
| [<span data-ttu-id="5eb3d-123">Usando a estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="5eb3d-123">Using Text Services Framework</span></span>](using-text-services-framework.md)<br/>         | <span data-ttu-id="5eb3d-124">Informações sobre como usar a estrutura de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-124">Information about using Text Services Framework.</span></span><br/>                                                      |
| [<span data-ttu-id="5eb3d-125">Referência da estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="5eb3d-125">Text Services Framework Reference</span></span>](text-services-framework-reference.md)<br/> | <span data-ttu-id="5eb3d-126">Documentação sobre interfaces de estrutura de serviços de texto, métodos, estruturas e outros elementos de código.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-126">Documentation about Text Services Framework interfaces, methods, structures, and other code elements.</span></span><br/> |
| [<span data-ttu-id="5eb3d-127">Glossário</span><span class="sxs-lookup"><span data-stu-id="5eb3d-127">Glossary</span></span>](glossary.md)<br/>                                                   | <span data-ttu-id="5eb3d-128">Lista alfabética de termos técnicos usados nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-128">Alphabetical listing of technical terms used in this documentation.</span></span><br/>                                   |



 

## <a name="additional-resources"></a><span data-ttu-id="5eb3d-129">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5eb3d-129">Additional resources</span></span>

<span data-ttu-id="5eb3d-130">O que você deve saber antes de ler este guia</span><span class="sxs-lookup"><span data-stu-id="5eb3d-130">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="5eb3d-131">Para os fins da ajuda da estrutura de serviços de texto, o termo "aplicativo" refere-se a um aplicativo habilitado para TSF, o termo "serviço de texto" refere-se a um serviço de texto do TSF e o termo "gerente" refere-se ao Gerenciador do TSF.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-131">For the purposes of the Text Services Framework Help, the term "application" refers to a TSF-enabled application, the term "text service" refers to a TSF text service, and the term "manager" refers to the TSF manager.</span></span> <span data-ttu-id="5eb3d-132">Cada termo aplica-se como mencionado neste documento, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-132">Each term applies as stated herein unless otherwise specified.</span></span> <span data-ttu-id="5eb3d-133">Os provedores de serviço de texto devem fornecer assinaturas digitais com seus executáveis binários.</span><span class="sxs-lookup"><span data-stu-id="5eb3d-133">Text service providers should provide digital signatures with their binary executables.</span></span>

 

 





