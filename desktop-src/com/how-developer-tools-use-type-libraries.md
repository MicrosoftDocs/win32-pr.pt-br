---
title: Como Ferramentas para Desenvolvedores usar bibliotecas de tipos
description: Como Ferramentas para Desenvolvedores usar bibliotecas de tipos
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105791612"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="c3b77-103">Como Ferramentas para Desenvolvedores usar bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="c3b77-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="c3b77-104">O diagrama a seguir ilustra como as várias ferramentas de desenvolvimento interagem com uma biblioteca de tipos do objeto COM.</span><span class="sxs-lookup"><span data-stu-id="c3b77-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="c3b77-105">Cada biblioteca de tipos expõe as interfaces padrão programáticas que as ferramentas podem chamar para obter informações sobre os elementos descritos nessa biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c3b77-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="c3b77-106">Neste diagrama, GUID significa identificador global exclusivo e RPC para chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="c3b77-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Diagrama que mostra como a ferramenta de desenvolvimento interage com uma biblioteca de tipos do objeto C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="c3b77-108">No diagrama anterior, as ferramentas de conversão de C++, como o compilador MIDL e os assistentes fornecidos pelo sistema de desenvolvimento de Microsoft Visual C++, geram arquivos de cabeçalho e stub.</span><span class="sxs-lookup"><span data-stu-id="c3b77-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="c3b77-109">Você pode adicionar esses arquivos ao seu projeto para usar o objeto COM descrito pela biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c3b77-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="c3b77-110">Da mesma forma, em Java, as ferramentas de desenvolvedor geram arquivos de classe e origem Java, que podem ser importados em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3b77-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="c3b77-111">Em Visual Basic, o cenário é um pouco mais simples.</span><span class="sxs-lookup"><span data-stu-id="c3b77-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="c3b77-112">Você não precisa gerar arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c3b77-112">You do not need to generate additional files.</span></span> <span data-ttu-id="c3b77-113">O ambiente de Visual Basic fornece caixas de diálogo que listam os objetos COM atualmente instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="c3b77-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="c3b77-114">Você seleciona o componente que deseja chamar do seu aplicativo e ele é adicionado ao seu projeto, seja como um componente ou uma referência.</span><span class="sxs-lookup"><span data-stu-id="c3b77-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="c3b77-115">O visualizador OLE-COM lê uma biblioteca de tipos, gera um arquivo IDL temporário com base na biblioteca de tipos e exibe-o para os usuários.</span><span class="sxs-lookup"><span data-stu-id="c3b77-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="c3b77-116">O visualizador OLE-COM também exibe a sintaxe C++ para os elementos COM listados na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c3b77-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="c3b77-117">Para obter mais informações sobre bibliotecas de tipos, consulte [bibliotecas de tipos e a linguagem de descrição de objeto](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="c3b77-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 