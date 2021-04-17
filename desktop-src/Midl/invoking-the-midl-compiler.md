---
title: Invocando o compilador MIDL
description: O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema. Consulte a opção/target para saber mais sobre as opções sugeridas e como gerar código otimizado para uma versão específica.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL do compilador MIDL, invocando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2019
ms.locfileid: "105751454"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="63fc4-105">Invocando o compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="63fc4-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="63fc4-106">O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema.</span><span class="sxs-lookup"><span data-stu-id="63fc4-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="63fc4-107">Consulte a opção [**/target**](-target.md) para saber mais sobre as opções sugeridas e como gerar código otimizado para uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="63fc4-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="63fc4-108">Execute o compilador MIDL na linha de comando usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="63fc4-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="63fc4-109"> *<  opções >* de MIDL **filename. idl**</span><span class="sxs-lookup"><span data-stu-id="63fc4-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="63fc4-110">onde *< ***as opções*** >* representam as opções de linha de comando que você deseja usar e filename. idl é o nome do arquivo MIDL a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="63fc4-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="63fc4-111">Uma lista completa dos comutadores e opções do compilador de MIDL está disponível quando você usa o compilador MIDL [**/Help**](-help-.md) e/?</span><span class="sxs-lookup"><span data-stu-id="63fc4-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="63fc4-112">comutadores.</span><span class="sxs-lookup"><span data-stu-id="63fc4-112">switches.</span></span> <span data-ttu-id="63fc4-113">As opções são organizadas por categorias.</span><span class="sxs-lookup"><span data-stu-id="63fc4-113">The switches are organized by categories.</span></span> <span data-ttu-id="63fc4-114">Para obter detalhes, consulte a [referência de Command-Line MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="63fc4-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="63fc4-115">O novo sinalizador global **$ (otimização de MIDL \_ )** existe no Win32. Mak.</span><span class="sxs-lookup"><span data-stu-id="63fc4-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="63fc4-116">Quando um arquivo. idl é compilado usando esse sinalizador, o stub gerado pode utilizar os recursos de RPC mais recentes disponíveis na plataforma especificada e, potencialmente, melhorar o desempenho e a estabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63fc4-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="63fc4-117">É recomendável que os aplicativos usem esse sinalizador ao usar MIDL.</span><span class="sxs-lookup"><span data-stu-id="63fc4-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="63fc4-118">**MIDL** **$ (otimização de MIDL \_ )** **...**</span><span class="sxs-lookup"><span data-stu-id="63fc4-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>