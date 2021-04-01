---
title: User-Defined recurso
description: Uma instrução de definição de recurso definida pelo usuário define um recurso que contém dados específicos do aplicativo.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- recurso definido pelo usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159747"
---
# <a name="user-defined-resource"></a><span data-ttu-id="33f12-104">User-Defined recurso</span><span class="sxs-lookup"><span data-stu-id="33f12-104">User-Defined Resource</span></span>

<span data-ttu-id="33f12-105">Uma instrução de definição de recurso definida pelo usuário define um recurso que contém dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="33f12-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="33f12-106">Os dados podem ter qualquer formato e podem ser definidos como o conteúdo de um determinado arquivo (se o parâmetro *filename* for fornecido) ou como uma série de números e cadeias de caracteres (se o bloco de *dados brutos* for especificado).</span><span class="sxs-lookup"><span data-stu-id="33f12-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="33f12-107">O *filename* especifica o nome de um arquivo que contém os dados binários do recurso.</span><span class="sxs-lookup"><span data-stu-id="33f12-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="33f12-108">O conteúdo do arquivo é incluído como o recurso.</span><span class="sxs-lookup"><span data-stu-id="33f12-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="33f12-109">O RC não interpreta os dados binários de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="33f12-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="33f12-110">É responsabilidade do programador garantir que os dados estejam corretamente alinhados à arquitetura do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="33f12-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="33f12-111">Um recurso definido pelo usuário também pode ser definido completamente no script de recurso usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="33f12-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="33f12-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33f12-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f12-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="33f12-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="33f12-114">Nome exclusivo ou um inteiro de 16 bits sem sinal que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="33f12-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="33f12-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*Identificação*</span><span class="sxs-lookup"><span data-stu-id="33f12-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="33f12-116">Nome exclusivo ou um inteiro de 16 bits sem sinal que identifica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="33f12-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="33f12-117">Se um número for fornecido, ele deverá ser maior que 255.</span><span class="sxs-lookup"><span data-stu-id="33f12-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="33f12-118">Os números de 1 a 255 são reservados para tipos de recursos redefinidos existentes e futuros.</span><span class="sxs-lookup"><span data-stu-id="33f12-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="33f12-119"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="33f12-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="33f12-120">Nome do arquivo que contém os dados do recurso.</span><span class="sxs-lookup"><span data-stu-id="33f12-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="33f12-121">O parâmetro deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="33f12-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="33f12-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*dados brutos*</span><span class="sxs-lookup"><span data-stu-id="33f12-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="33f12-123">Dados brutos que consistem em um ou mais números inteiros ou cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="33f12-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="33f12-124">Os inteiros podem ser especificados em formato decimal, octal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="33f12-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="33f12-125">Para ser compatível com o Windows de 16 bits, os inteiros são armazenados como valores de palavra.</span><span class="sxs-lookup"><span data-stu-id="33f12-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="33f12-126">Você pode armazenar um inteiro como um valor DWORD qualificando o inteiro com o sufixo "L".</span><span class="sxs-lookup"><span data-stu-id="33f12-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="33f12-127">As cadeias de caracteres são colocadas entre aspas.</span><span class="sxs-lookup"><span data-stu-id="33f12-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="33f12-128">O RC não acrescenta automaticamente um caractere nulo de terminação a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="33f12-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="33f12-129">Cada cadeia de caracteres é uma sequência dos caracteres ANSI especificados, a menos que você o qualifique como uma cadeia de caracteres largos com o prefixo "L".</span><span class="sxs-lookup"><span data-stu-id="33f12-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="33f12-130">O bloco de dados começa em um limite **DWORD** e o RC não executa nenhum preenchimento ou alinhamento de dados dentro do bloco de *dados brutos* .</span><span class="sxs-lookup"><span data-stu-id="33f12-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="33f12-131">É responsabilidade do programador garantir o alinhamento adequado dos dados dentro do bloco.</span><span class="sxs-lookup"><span data-stu-id="33f12-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="33f12-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="33f12-132">Example</span></span>

<span data-ttu-id="33f12-133">O exemplo a seguir mostra várias instruções definidas pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="33f12-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




