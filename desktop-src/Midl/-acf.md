---
title: comutador/ACF
description: A opção/ACF permite que o usuário forneça um nome de arquivo ACF explícito. A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- MIDL do comutador/ACF
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916797"
---
# <a name="acf-switch"></a><span data-ttu-id="b546a-105">comutador/ACF</span><span class="sxs-lookup"><span data-stu-id="b546a-105">/acf switch</span></span>

<span data-ttu-id="b546a-106">A opção **/ACF** permite que o usuário forneça um nome de arquivo ACF explícito.</span><span class="sxs-lookup"><span data-stu-id="b546a-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="b546a-107">A opção também permite o uso de nomes de interface diferentes nos arquivos IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="b546a-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="b546a-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="b546a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b546a-109">*\_nome de arquivo ACF*</span><span class="sxs-lookup"><span data-stu-id="b546a-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="b546a-110">Especifica o nome do ACF.</span><span class="sxs-lookup"><span data-stu-id="b546a-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="b546a-111">O espaço em branco pode ou não estar presente entre o comutador **/ACF** e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b546a-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b546a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b546a-112">Remarks</span></span>

<span data-ttu-id="b546a-113">Por padrão, o compilador MIDL constrói o nome do ACF substituindo a extensão de nome de arquivo IDL (normalmente. idl) por. ACF.</span><span class="sxs-lookup"><span data-stu-id="b546a-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="b546a-114">Quando a opção **/ACF** está presente, o ACF pega seu nome do nome de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b546a-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="b546a-115">A opção **/ACF** se aplica somente ao arquivo IDL especificado na linha de comando do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="b546a-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="b546a-116">Ele não se aplica a arquivos importados.</span><span class="sxs-lookup"><span data-stu-id="b546a-116">It does not apply to imported files.</span></span>

<span data-ttu-id="b546a-117">Quando a opção **/ACF** é usada, o nome da interface no ACF não precisa corresponder ao nome da interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="b546a-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="b546a-118">Esse recurso permite que as interfaces compartilhem uma especificação ACF.</span><span class="sxs-lookup"><span data-stu-id="b546a-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="b546a-119">Quando um caminho absoluto para um ACF não é especificado, o compilador MIDL pesquisa no diretório atual, nos diretórios fornecidos pela opção [**/i**](-i.md) e nos diretórios no caminho de inclusão.</span><span class="sxs-lookup"><span data-stu-id="b546a-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="b546a-120">Se o ACF não for encontrado, o compilador MIDL pressupõe que não há um ACF para essa interface.</span><span class="sxs-lookup"><span data-stu-id="b546a-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="b546a-121">Para obter mais informações sobre a sequência de diretórios, consulte as entradas de referência para as opções [**/i**](-i.md) e [**/. \_ \_ Idir def**](-no-def-idir.md) .</span><span class="sxs-lookup"><span data-stu-id="b546a-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="b546a-122">Para obter mais informações relacionadas ao **/ACF**, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="b546a-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b546a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b546a-123">Examples</span></span>

<span data-ttu-id="b546a-124">**MIDL/ACF bar. ACF filename. idl**</span><span class="sxs-lookup"><span data-stu-id="b546a-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b546a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b546a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b546a-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="b546a-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="b546a-127">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="b546a-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b546a-128">**/. de \_ \_ Idir def**</span><span class="sxs-lookup"><span data-stu-id="b546a-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




