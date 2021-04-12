---
title: Salvando a saída do pré-processador
description: A exibição da saída do pré-processador pode ser um método eficaz de solução de problemas, como quando ocorre uma sintaxe IDL, C ou C-pré-processador inválida, ou quando valores falsos-D na linha de comando MIDL resultam em erros de misteriosos de relatório de MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL do compilador MIDL, salvando a saída do pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364115"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="b4fbb-104">Salvando a saída do pré-processador</span><span class="sxs-lookup"><span data-stu-id="b4fbb-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="b4fbb-105">A exibição da saída do pré-processador pode ser um método eficaz de solução de problemas, como quando ocorre uma sintaxe IDL, C ou C-pré-processador inválida, ou quando valores falsos-D na linha de comando MIDL resultam em erros de misteriosos de relatório de MIDL.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="b4fbb-106">Os desenvolvedores também podem querer examinar a saída do pré-processador para determinar quais arquivos e definições estavam presentes no fluxo de entrada do compilador, como quando um caso difícil do conflito de redefinição de tipo deve ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="b4fbb-107">Ou menos comumente, alguns desenvolvedores podem querer forçar comutadores privados no pré-processador com [**/cpp \_ opt**](-cpp-opt.md)ou talvez queiram ver como funcionam as opções.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="b4fbb-108">A maneira mais fácil e menos invasiva de obter arquivos pré-processados de uma execução de compilação MIDL é usar a opção [**-savePP**](-savepp.md) .</span><span class="sxs-lookup"><span data-stu-id="b4fbb-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="b4fbb-109">A opção **-savePP** simplesmente impede o MIDL de excluir os arquivos temporários que o pré-processador passa de volta para o MIDL.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="b4fbb-110">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fbb-110">Consider the following:</span></span>

<span data-ttu-id="b4fbb-111">**MIDL-savePP-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1-Oicf-env Win32 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="b4fbb-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="b4fbb-112">Essa diretiva compila stub. idl, mas preserva todos os arquivos de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="b4fbb-113">O MIDL gera execuções de pré-processador separadas para o arquivo IDL e ACF (se presente), bem como para todos os arquivos importados.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="b4fbb-114">Para uma compilação de DCOM, vários arquivos de pré-processador são geralmente produzidos, mesmo que sejam processados pelo MIDL como um fluxo de entrada contíguo virtual.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="b4fbb-115">Em um ambiente de programação típico do Windows, os arquivos temporários podem ser encontrados no diretório Temp como nomes de arquivos, como MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="b4fbb-116">Se estiver preservando a saída do pré-processador, é uma prática recomendada observar os arquivos recentes no diretório Temp para identificar quais arquivos estão associados ao pré-processador executado.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="b4fbb-117">Em casos simples, como quando o arquivo IDL compilado não importa outros arquivos direta ou indiretamente, ou ao examinar o arquivo de nível superior, o pré-processador pode ser invocado diretamente.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="b4fbb-118">Executar o pré-processador do C/C++ diretamente pode revelar erros mascarados ou confusos pelo MIDL.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="b4fbb-119">Por exemplo, as duas linhas de comando de pré-processador a seguir podem ser usadas para a linha MIDL citada anteriormente:</span><span class="sxs-lookup"><span data-stu-id="b4fbb-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="b4fbb-120">**CL/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**</span><span class="sxs-lookup"><span data-stu-id="b4fbb-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="b4fbb-121">**CL/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="b4fbb-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="b4fbb-122">No primeiro desses dois exemplos, **/e** [**/nologo**](-nologo.md) são as opções que o MIDL adiciona ao invocar o pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="b4fbb-123">A saída do pré-processador é enviada para stdout (a tela) e, portanto, requer o redirecionamento para um arquivo para exame.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="b4fbb-124">No segundo desses exemplos, **/p** direciona o pré-processador para redirecionar a saída para um \* arquivo. i; nesse caso, um arquivo stub. i seria criado no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="b4fbb-125">A opção [**/cpp \_ opt**](-cpp-opt.md) também pode ser usada para obter um arquivo pré-processado, mas é difícil e inferior aos métodos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="b4fbb-126">O exemplo a seguir também produz um arquivo stub. i, como fazia o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="b4fbb-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="b4fbb-127">As aspas no exemplo a seguir são essenciais:</span><span class="sxs-lookup"><span data-stu-id="b4fbb-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="b4fbb-128">**MIDL-Oicf-Win32-cpp \_ opt "/E/p-ID: \\ NT \\ Public \\ SDK \\ Inc-DNTENV = 1" stub. idl**</span><span class="sxs-lookup"><span data-stu-id="b4fbb-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




