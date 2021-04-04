---
title: Requisitos de pré-processador do C para MIDL
description: Esta página se aplica somente a desenvolvedores que têm motivos específicos para substituir o pré-processador do Microsoft C/C++ como o pré-processador usado pelo MIDL ou para os desenvolvedores que devem especificar comutadores de pré-processador personalizados.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL do compilador MIDL, pré-processador, requisitos
- C-pré-processador MIDL, requisitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916499"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="a534f-105">Requisitos de pré-processador do C para MIDL</span><span class="sxs-lookup"><span data-stu-id="a534f-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="a534f-106">Esta página se aplica somente a desenvolvedores que têm motivos específicos para substituir o pré-processador do Microsoft C/C++ como o pré-processador usado pelo MIDL ou para os desenvolvedores que devem especificar comutadores de pré-processador personalizados.</span><span class="sxs-lookup"><span data-stu-id="a534f-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="a534f-107">O MIDL alterna [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)e [**// \_ ///////////////////////**](-no-cpp-nocpp.md)</span><span class="sxs-lookup"><span data-stu-id="a534f-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="a534f-108">Normalmente, não há motivo para substituir o pré-processador do Microsoft C/C++, nem para especificar comutadores de pré-processador personalizados.</span><span class="sxs-lookup"><span data-stu-id="a534f-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="a534f-109">O compilador MIDL usa um pré-processador C durante o processamento inicial do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a534f-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="a534f-110">O ambiente de compilação usado durante a compilação dos arquivos IDL é associado a um pré-processador C/C++ padrão.</span><span class="sxs-lookup"><span data-stu-id="a534f-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="a534f-111">Se um pré-processador diferente for usado, o compilador MIDL switch [**/cpp \_ cmd**](-cpp-cmd.md) permitirá uma substituição do nome padrão C/C++-preprocessador:</span><span class="sxs-lookup"><span data-stu-id="a534f-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="a534f-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nome do pré-processador \_*</span><span class="sxs-lookup"><span data-stu-id="a534f-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="a534f-113">Especifica o nome do pré-processador a ser usado pelo MIDL.</span><span class="sxs-lookup"><span data-stu-id="a534f-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="a534f-114">Pode ser especificado com um caminho para o binário.</span><span class="sxs-lookup"><span data-stu-id="a534f-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="a534f-115">A extensão. exe é opcional.</span><span class="sxs-lookup"><span data-stu-id="a534f-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a534f-116"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="a534f-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a534f-117">Especifica o nome do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="a534f-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="a534f-118">O compilador MIDL espera que qualquer pré-processador Observe as seguintes convenções:</span><span class="sxs-lookup"><span data-stu-id="a534f-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="a534f-119">O arquivo de entrada é especificado como o último argumento na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a534f-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="a534f-120">O pré-processador deve redirecionar a saída para o dispositivo de saída padrão, stdout.</span><span class="sxs-lookup"><span data-stu-id="a534f-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="a534f-121">No fluxo de saída do pré-processador, as diretivas de **\# linha** estão presentes para habilitar melhores mensagens de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a534f-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="a534f-122">As diretivas de linha são as únicas diretivas de pré-processador no fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="a534f-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="a534f-123">O MIDL pressupõe que o pré-processador gerado removeu todas as diretivas de pré-processador do fluxo de entrada do compilador, com exceção das ocorrências da diretiva de linha necessária para indicar o local de origem nas mensagens do compilador.</span><span class="sxs-lookup"><span data-stu-id="a534f-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="a534f-124">Ao indicar um pré-processador diferente do pré-processador do Microsoft C/C++, ou ao especificar opções de pré-processador com a opção [**/cpp \_ opt**](-cpp-opt.md) , a especificação de uma opção de pré-processador apropriada que coloca as diretivas de linha no fluxo de entrada do compilador é necessária.</span><span class="sxs-lookup"><span data-stu-id="a534f-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="a534f-125">Por exemplo, para o pré-processador do Microsoft C/C++, a opção **/e** teria que ser usada:</span><span class="sxs-lookup"><span data-stu-id="a534f-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="a534f-126">A diretiva de **\# linha** é aceita pelo MIDL em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="a534f-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="a534f-127">Para obter uma descrição completa da diretiva de linha e outras diretivas de pré-processador, consulte a documentação do compilador C que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a534f-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="a534f-128">MIDL aceita apenas a diretiva de pré-processador de linha.</span><span class="sxs-lookup"><span data-stu-id="a534f-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="a534f-129">Portanto, se a opção de [**\_ cpp de///**](-no-cpp-nocpp.md) não tiver sido usada, o arquivo de entrada não deverá ter outras diretivas de pré-processador ou o arquivo de entrada deverá ter sido processado antes de invocar MIDL.</span><span class="sxs-lookup"><span data-stu-id="a534f-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="a534f-130">Para obter mais informações, consulte [lidando com as \# definições em arquivos IDL](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="a534f-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




