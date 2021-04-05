---
title: Opção/i
description: A opção/I especifica os diretórios a serem pesquisados em busca de arquivos IDL importados, arquivos de cabeçalho incluídos e arquivos ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I alternar MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006640"
---
# <a name="i-switch"></a><span data-ttu-id="fcf8a-104">Opção/i</span><span class="sxs-lookup"><span data-stu-id="fcf8a-104">/I switch</span></span>

<span data-ttu-id="fcf8a-105">A opção **/i** especifica os diretórios a serem pesquisados em busca de arquivos IDL importados, arquivos de cabeçalho incluídos e arquivos ACF.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="fcf8a-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="fcf8a-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fcf8a-107">*caminho de inclusão \_*</span><span class="sxs-lookup"><span data-stu-id="fcf8a-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="fcf8a-108">Especifica um ou mais diretórios que contêm arquivos de importação, inclusão e ACF.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="fcf8a-109">O espaço em branco entre a opção **/i** e o *\_ caminho de inclusão* é opcional.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="fcf8a-110">Separe vários diretórios com um caractere de ponto-e-vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="fcf8a-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcf8a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcf8a-111">Remarks</span></span>

<span data-ttu-id="fcf8a-112">Mais de um diretório pode aparecer com cada opção **/i** e mais de uma opção **/i** pode aparecer com cada invocação de compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="fcf8a-113">Os diretórios são pesquisados na ordem em que são especificados.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="fcf8a-114">A configuração da opção **/i** também é passada pelo compilador MIDL para o pré-processador c do compilador c.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="fcf8a-115">Quando a [**opção \_ /cpp cmd**](-cpp-cmd.md) está presente e a opção de [**/cpp \_ opt**](-cpp-opt.md) não é, o compilador MIDL concatena a cadeia de caracteres especificada pela opção **\_ cmd/cpp** com as opções **/i**, [**/d**](-d.md)e [**/U**](-u.md) e usa essa cadeia de caracteres concatenada para invocar o pré-processador C para cada arquivo de origem IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="fcf8a-116">A opção de compilador de MIDL **/i** não é passada para o pré-processador quando o parâmetro de compilador MIDL switch/ **/cpp \_ opt** é especificado. **\_**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="fcf8a-117">Em ambientes de sistema operacional da Microsoft (Windows de 64 bits, Windows de 32 bits, Windows de 16 bits e MS-DOS), os diretórios são pesquisados na seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="fcf8a-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="fcf8a-118">Diretório atual</span><span class="sxs-lookup"><span data-stu-id="fcf8a-118">Current directory</span></span>
2.  <span data-ttu-id="fcf8a-119">Diretórios especificados pela opção **/i** (na ordem em que seguem a opção)</span><span class="sxs-lookup"><span data-stu-id="fcf8a-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="fcf8a-120">Diretórios especificados pela variável de ambiente INCLUDE</span><span class="sxs-lookup"><span data-stu-id="fcf8a-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="fcf8a-121">Quando os diretórios são especificados com a opção **/i** , a opção de [**\_ \_ Idir**](-no-def-idir.md) de chave de alteração instrui o compilador MIDL a ignorar o diretório atual, ignorar os diretórios especificados pela variável de ambiente include e Pesquisar apenas os diretórios especificados.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="fcf8a-122">Quando nenhum diretório é especificado com a opção **/i** , a opção de [**\_ \_ Idir de//**](-no-def-idir.md) chave de alteração instrui o compilador MIDL a pesquisar somente o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="fcf8a-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="fcf8a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fcf8a-123">Examples</span></span>

<span data-ttu-id="fcf8a-124">**MIDL/I c: \\ include; c: \\ include \\ h/i \\ include2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fcf8a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcf8a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf8a-126">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="fcf8a-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fcf8a-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="fcf8a-128">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="fcf8a-129">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="fcf8a-130">**/. de \_ \_ Idir def**</span><span class="sxs-lookup"><span data-stu-id="fcf8a-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




