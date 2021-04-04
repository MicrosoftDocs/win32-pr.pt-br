---
title: Guias de desenvolvedor do Windows Ribbon Framework
description: Os tópicos contidos nesta seção descrevem aspectos específicos do Windows Ribbon Framework.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Faixa de Ribbon do Windows, estrutura
- Faixa de Ribbon, estrutura
- Faixa de-se do Windows, guias de desenvolvedor
- Faixa de guia, guias de desenvolvedor
- guias do desenvolvedor para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084801"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="d88f4-108">Guias de desenvolvedor do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d88f4-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="d88f4-109">Os tópicos contidos nesta seção descrevem aspectos específicos do Windows Ribbon Framework.</span><span class="sxs-lookup"><span data-stu-id="d88f4-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="d88f4-110">Noções básicas</span><span class="sxs-lookup"><span data-stu-id="d88f4-110">Basics</span></span>

[<span data-ttu-id="d88f4-111">Criando um aplicativo de faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="d88f4-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="d88f4-112">Para que o Windows Ribbon Framework consuma o arquivo de marcação da faixa de faixas, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.</span><span class="sxs-lookup"><span data-stu-id="d88f4-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="d88f4-113">Um compilador de marcação de faixa de medida dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d88f4-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="d88f4-114">Além de compilar a versão binária da marcação da faixa de faixas, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="d88f4-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="d88f4-115">Migrando para o Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d88f4-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="d88f4-116">Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando da estrutura da faixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d88f4-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="d88f4-117">Essa é uma maneira fácil e eficaz de modernizar e revitalize o aplicativo ao mesmo tempo em que também melhora a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d88f4-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="d88f4-118">Noções básicas sobre comandos e controles</span><span class="sxs-lookup"><span data-stu-id="d88f4-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="d88f4-119">A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comando da estrutura da faixa de uma, um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d88f4-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="d88f4-120">Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="d88f4-120">User Interface</span></span>

[<span data-ttu-id="d88f4-121">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="d88f4-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="d88f4-122">Como um sistema de apresentação de comando avançado, a estrutura da faixa de faixas foi projetada para dar suporte extensiva a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d88f4-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="d88f4-123">Todos os recursos de imagem são declarados na [marcação da faixa](windowsribbon-schema.md) de lista ou consultados de um aplicativo host da faixa de Ribbon.</span><span class="sxs-lookup"><span data-stu-id="d88f4-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="d88f4-124">Para o Windows 8 e posterior, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network Graphics) com transparência.</span><span class="sxs-lookup"><span data-stu-id="d88f4-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="d88f4-125">Para o Windows 7 e versões anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado no Windows.</span><span class="sxs-lookup"><span data-stu-id="d88f4-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="d88f4-126">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="d88f4-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="d88f4-127">Os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout que são impostas pela estrutura da faixa de opções e com base em uma combinação de comportamentos padrão e modelos de layout (ambos definidos pelo Framework e personalizados), conforme declarado na marcação da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d88f4-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="d88f4-128">Essas regras definem os comportamentos de layout adaptável da estrutura da faixa de opção que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opção em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d88f4-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="d88f4-129">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="d88f4-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="d88f4-130">A estrutura da faixa de tipos fornece aos desenvolvedores um modelo robusto e consistente para o gerenciamento de conteúdo dinâmico em uma variedade de controles baseados em coleção.</span><span class="sxs-lookup"><span data-stu-id="d88f4-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="d88f4-131">Ao adaptar e reconfigurar a interface do usuário da faixa de opções (IU), esses controles dinâmicos permitem que a estrutura responda à interação do usuário tanto no aplicativo host quanto na faixa de opções e forneça a flexibilidade para lidar com vários ambientes de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d88f4-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="d88f4-132">Exibindo guias contextuais</span><span class="sxs-lookup"><span data-stu-id="d88f4-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="d88f4-133">Em um aplicativo do Framework da faixa de das, uma guia contextual é um controle de [guia](windowsribbon-controls-tab.md) oculto que é exibido na linha da guia quando um objeto no espaço de trabalho do aplicativo, como uma imagem, é selecionado ou realçado.</span><span class="sxs-lookup"><span data-stu-id="d88f4-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="d88f4-134">Reconfiguração da faixa de modo com modos de aplicativo</span><span class="sxs-lookup"><span data-stu-id="d88f4-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="d88f4-135">A estrutura da faixa de faixas é compatível com a reconfiguração dinâmica e a exposição de elementos principais da interface do usuário da faixa de medida (IU) em tempo de execução, com base no estado do aplicativo (também conhecido como contexto).</span><span class="sxs-lookup"><span data-stu-id="d88f4-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="d88f4-136">Declarados e associados a elementos específicos na marcação, os vários Estados com suporte de um aplicativo são chamados de modos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d88f4-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="d88f4-137">Personalizando cores da faixa de das</span><span class="sxs-lookup"><span data-stu-id="d88f4-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="d88f4-138">A estrutura da faixa de faixas expõe um conjunto de propriedades de cores que permite a um aplicativo personalizar a aparência de vários elementos da interface do usuário da faixa de faixas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d88f4-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="d88f4-139">Exibindo a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="d88f4-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="d88f4-140">A estrutura da faixa de forma expõe um conjunto de propriedades que permite que um aplicativo especifique como a interface do usuário da faixa de forma (IU) é exibida em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d88f4-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="d88f4-141">Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d88f4-141">Management</span></span>

[<span data-ttu-id="d88f4-142">Estado da faixa de medida persistente</span><span class="sxs-lookup"><span data-stu-id="d88f4-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="d88f4-143">O Windows Ribon Framework (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d88f4-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="d88f4-144">Escutando eventos da faixa de das</span><span class="sxs-lookup"><span data-stu-id="d88f4-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="d88f4-145">A estrutura da faixa de faixas usa a infraestrutura do [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de forma do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d88f4-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="d88f4-146">Compilador de marcação</span><span class="sxs-lookup"><span data-stu-id="d88f4-146">Markup Compiler</span></span>

[<span data-ttu-id="d88f4-147">Compilando marcação da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="d88f4-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="d88f4-148">Para que a estrutura da faixa de faixas consuma o arquivo de [marcação da faixa de faixas](windowsribbon-schema.md) , o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.</span><span class="sxs-lookup"><span data-stu-id="d88f4-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="d88f4-149">Um compilador de marcação dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="d88f4-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="d88f4-150">Além de compilar a versão binária da marcação, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="d88f4-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="d88f4-151">Compreendendo as mensagens do compilador de marcação</span><span class="sxs-lookup"><span data-stu-id="d88f4-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="d88f4-152">O compilador de marcação do Windows Ribbon Framework (faixa de opções), o compilador de comando da interface do usuário (UICC.exe), valida a marcação da faixa de opções em relação ao esquema da faixa e um conjunto adicional de regras definidas pela estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d88f4-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 