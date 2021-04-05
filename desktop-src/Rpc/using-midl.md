---
title: Usando MIDL
description: Criar e compilar uma interface linguagem IDL da Microsoft (MIDL) e uma chamada de procedimento remoto (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641778"
---
# <a name="using-midl"></a><span data-ttu-id="77f33-103">Usando MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-103">Using MIDL</span></span>

<span data-ttu-id="77f33-104">Todas as interfaces para programas que usam RPC devem ser definidas em linguagem IDL da Microsoft (MIDL) e compiladas com o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="77f33-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="77f33-105">Os tópicos a seguir apresentam uma breve visão geral da criação e da compilação de uma interface MIDL:</span><span class="sxs-lookup"><span data-stu-id="77f33-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="77f33-106">Definindo uma interface com MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="77f33-107">Compilando um arquivo MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="77f33-108">Para obter uma discussão detalhada sobre esses tópicos, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="77f33-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="77f33-109">Definindo uma interface com MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="77f33-110">Os arquivos MIDL são arquivos de texto que você pode criar e editar com um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="77f33-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="77f33-111">Se você gerar um UUID para sua interface, você normalmente armazenará a saída em um arquivo MIDL de modelo.</span><span class="sxs-lookup"><span data-stu-id="77f33-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="77f33-112">Para obter mais informações sobre UUIDs, consulte [gerando UUIDs de interface](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="77f33-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="77f33-113">Todas as interfaces no MIDL seguem o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="77f33-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="77f33-114">Eles começam com um cabeçalho que contém uma lista de atributos de interface e o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="77f33-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="77f33-115">Os atributos são colocados entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="77f33-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="77f33-116">O cabeçalho da interface é seguido por seu corpo, que é colocado entre chaves.</span><span class="sxs-lookup"><span data-stu-id="77f33-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="77f33-117">Uma interface simples é mostrada no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="77f33-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="77f33-118">Alguns dos atributos que normalmente aparecem em uma definição de interface MIDL são o UUID e o número de versão da interface.</span><span class="sxs-lookup"><span data-stu-id="77f33-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="77f33-119">O corpo da definição de interface deve conter as declarações de procedimento de todos os procedimentos remotos na interface.</span><span class="sxs-lookup"><span data-stu-id="77f33-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="77f33-120">Ele também pode conter as declarações de tipos de dados e constantes exigidas pela interface.</span><span class="sxs-lookup"><span data-stu-id="77f33-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="77f33-121">Todos os parâmetros nas declarações de procedimento remoto devem ser declarados como \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="77f33-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="77f33-122">Essas declarações especificam que o programa cliente passa dados para um procedimento remoto, obtém dados de um procedimento remoto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="77f33-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="77f33-123">Para obter informações mais detalhadas sobre declarações de parâmetro de interface, consulte [o corpo da interface IDL](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="77f33-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="77f33-124">Compilando um arquivo MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-124">Compiling a MIDL File</span></span>

<span data-ttu-id="77f33-125">O compilador MIDL é uma ferramenta de linha de comando que é instalada automaticamente com o SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="77f33-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="77f33-126">Invoque-o em uma janela de comando digitando o comando **MIDL**, seguido pelo nome de um arquivo MIDL, na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="77f33-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="77f33-127">Verifique se o diretório que contém o compilador MIDL está em seu caminho.</span><span class="sxs-lookup"><span data-stu-id="77f33-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="77f33-128">O exemplo a seguir ilustra seu uso:</span><span class="sxs-lookup"><span data-stu-id="77f33-128">The following example illustrates its use:</span></span>

<span data-ttu-id="77f33-129">**MIDL MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="77f33-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="77f33-130">Observe que você não precisa incluir a extensão se o nome do arquivo tiver a extensão. idl.</span><span class="sxs-lookup"><span data-stu-id="77f33-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="77f33-131">Você também pode usar as opções de [linha de comando](/windows/desktop/Midl/midl-command-line-reference) do compilador MIDL inserindo-as entre o comando **MIDL** e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="77f33-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="77f33-132">Isso é demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="77f33-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="77f33-133">**MIDL/ACF MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="77f33-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="77f33-134">Neste exemplo, o compilador MIDL é executado usando o arquivo MyApp. idl como o arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="77f33-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="77f33-135">A opção de linha de comando **/ACF** instrui o compilador a usar um ACF (arquivo de configuração de aplicativo) para entrada também.</span><span class="sxs-lookup"><span data-stu-id="77f33-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="77f33-136">Os arquivos de configuração de aplicativo são discutidos mais detalhadamente nos [arquivos IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="77f33-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="77f33-137">Para obter informações mais detalhadas sobre como usar o compilador MIDL, consulte o [linguagem IDL da Microsoft (MIDL)](/windows/desktop/Midl/midl-start-page), que contém informações sobre os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="77f33-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="77f33-138">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="77f33-139">C/C++-considerações do compilador</span><span class="sxs-lookup"><span data-stu-id="77f33-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="77f33-140">Arquivos gerados para uma interface RPC</span><span class="sxs-lookup"><span data-stu-id="77f33-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="77f33-141">Referência de linha de comando MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="77f33-142">Referência da linguagem MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="77f33-143">Erros e avisos do compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="77f33-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 