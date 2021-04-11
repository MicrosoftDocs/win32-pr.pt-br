---
title: atributo de importação
description: A diretiva de importação especifica outro arquivo IDL, ODL ou Header que contém as definições que você deseja referenciar do seu arquivo IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- importar atributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293937"
---
# <a name="import-attribute"></a><span data-ttu-id="b9b0a-104">atributo de importação</span><span class="sxs-lookup"><span data-stu-id="b9b0a-104">import attribute</span></span>

<span data-ttu-id="b9b0a-105">A diretiva de **importação** especifica outro arquivo IDL, ODL ou Header que contém as definições que você deseja referenciar do seu arquivo IDL principal.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="b9b0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9b0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9b0a-107">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="b9b0a-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="b9b0a-108">Especifica o nome do arquivo de cabeçalho, IDL ou ODL a ser importado.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9b0a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9b0a-109">Remarks</span></span>

<span data-ttu-id="b9b0a-110">Com a diretiva **Import** , todas as instruções IDL no arquivo importado, como TYPEDEFs, declarações de constantes e definições de interface, ficam disponíveis para a importação. Arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="b9b0a-111">O arquivo importado é processado separadamente (o que significa que o pré-processador de CPP é invocado de forma independente) do arquivo de importação de IDL.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="b9b0a-112">Dessa forma, as diretivas anteriores ao processador, como \# definir, não são transferidas de um cabeçalho ou arquivo IDL importado para o arquivo IDL de importação.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="b9b0a-113">Assim como a macro de pré-processador de linguagem C, a diretiva de **importação** informa o compilador **\# para incluir tipos** de dados que foram definidos nos arquivos IDL importados.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="b9b0a-114">Ao contrário da diretiva **\# include** , a diretiva de **importação** ignora os protótipos de procedimento, pois nenhum stub é gerado para qualquer coisa no arquivo importado.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="b9b0a-115">Para obter informações específicas sobre como usar a **importação** para incluir arquivos de cabeçalho em um arquivo IDL, consulte [Importando arquivos de cabeçalho do sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="b9b0a-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="b9b0a-116">O cabeçalho do idioma C (. H) gerado para a interface não contém diretamente os tipos importados, mas, em vez disso, gera uma diretiva **\# include** para o arquivo de cabeçalho correspondente à interface importada.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="b9b0a-117">Por exemplo, quando você importa BASE. IDL em seu derivado. IDL, o arquivo de cabeçalho gerado derivado. H conterá a diretiva **\# include** base. H.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="b9b0a-118">As seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="b9b0a-118">The following rules apply:</span></span>

-   <span data-ttu-id="b9b0a-119">A palavra-chave de **importação** é opcional e pode aparecer zero ou mais vezes no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="b9b0a-120">Cada palavra-chave de **importação** pode ser associada a mais de um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="b9b0a-121">Separe vários nomes de arquivo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="b9b0a-122">Você deve colocar o nome do arquivo entre aspas e encerrar a instrução de importação com um ponto-e-vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="b9b0a-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="b9b0a-123">Você pode importar uma interface que não tem atributos para outro arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="b9b0a-124">No entanto, a interface deve conter apenas tipos de texto; Ele não pode conter nenhum procedimento.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="b9b0a-125">Se até um procedimento estiver contido na interface importada, você deverá especificar um atributo [**local**](local.md) ou [**UUID**](uuid.md) .</span><span class="sxs-lookup"><span data-stu-id="b9b0a-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="b9b0a-126">A função de **importação** é idempotentÂ â € ", ou seja, a importação de uma interface mais de uma vez não tem nenhum efeito adicional.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="b9b0a-127">O comportamento da diretiva de **importação** é independente do modo de compilador de MIDL alternar [**/MS \_ ext**](-ms-ext.md) (o padrão), [**/OSF**](-osf.md)e [**/app \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="b9b0a-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="b9b0a-128">No entanto, o modo de compilador (**/OSF** ou **/MS \_ ext**) pode afetar a decoração de atributo de ponteiro em tipos importados.</span><span class="sxs-lookup"><span data-stu-id="b9b0a-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="b9b0a-129">Para obter detalhes [, consulte herança de tipo de atributo de ponteiro](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="b9b0a-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="b9b0a-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9b0a-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="b9b0a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9b0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b0a-132">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="b9b0a-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-133">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="b9b0a-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b9b0a-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-135">**incluir**</span><span class="sxs-lookup"><span data-stu-id="b9b0a-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-136">Importar arquivos de cabeçalho do sistema</span><span class="sxs-lookup"><span data-stu-id="b9b0a-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-137">Importando arquivos e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="b9b0a-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-138">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="b9b0a-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="b9b0a-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b9b0a-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 