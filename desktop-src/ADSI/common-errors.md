---
title: Erros comuns (ADSI)
description: Todos os erros específicos de ADSI têm uma forma hexadecimal de 80005xxx. Os códigos de erro mais comuns encontrados são descritos na tabela a seguir.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104293686"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="180fb-104">Erros comuns (ADSI)</span><span class="sxs-lookup"><span data-stu-id="180fb-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="180fb-105">Todos os erros específicos de ADSI têm uma forma hexadecimal de 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="180fb-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="180fb-106">Os códigos de erro mais comuns encontrados são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="180fb-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="180fb-107">Código de erro hexadecimal ADSI</span><span class="sxs-lookup"><span data-stu-id="180fb-107">ADSI hex error code</span></span> | <span data-ttu-id="180fb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="180fb-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180fb-109">80005000</span><span class="sxs-lookup"><span data-stu-id="180fb-109">80005000</span></span><br/> | <span data-ttu-id="180fb-110">Um nome de caminho ADSI inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="180fb-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="180fb-111">Esse erro resulta da transmissão de um ADsPath mal formado para **GetObject** durante a associação a um objeto.</span><span class="sxs-lookup"><span data-stu-id="180fb-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="180fb-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="180fb-112">8000500D</span></span><br/> | <span data-ttu-id="180fb-113">A propriedade ADSI não pode ser encontrada no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="180fb-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="180fb-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="180fb-114">8000500E</span></span><br/> | <span data-ttu-id="180fb-115">O objeto ADSI existe.</span><span class="sxs-lookup"><span data-stu-id="180fb-115">The ADSI object exists.</span></span> <span data-ttu-id="180fb-116">Se você tentar criar um objeto ADSI com o mesmo nome de um objeto ADSI existente, esse erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="180fb-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="180fb-117">Para obter uma lista completa de códigos de erro ADSI, consulte [códigos de erro genéricos da ADSI](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="180fb-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="180fb-118">Erros COM</span><span class="sxs-lookup"><span data-stu-id="180fb-118">COM Errors</span></span>

<span data-ttu-id="180fb-119">Como a ADSI é composta de objetos COM, ela retornará códigos de erro padrão COM.</span><span class="sxs-lookup"><span data-stu-id="180fb-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="180fb-120">A tabela a seguir lista os códigos de erro COM mais comumente encontrados na programação ADSI.</span><span class="sxs-lookup"><span data-stu-id="180fb-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="180fb-121">Código de erro HEX COM</span><span class="sxs-lookup"><span data-stu-id="180fb-121">COM hex error code</span></span>  | <span data-ttu-id="180fb-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="180fb-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180fb-123">80004005</span><span class="sxs-lookup"><span data-stu-id="180fb-123">80004005</span></span><br/> | <span data-ttu-id="180fb-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="180fb-124">Unspecified error.</span></span> <span data-ttu-id="180fb-125">A causa da falha do objeto COM é indeterminada pela ADSI.</span><span class="sxs-lookup"><span data-stu-id="180fb-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="180fb-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="180fb-126">800041E4</span></span><br/> | <span data-ttu-id="180fb-127">Objeto não localizado.</span><span class="sxs-lookup"><span data-stu-id="180fb-127">Object not found.</span></span> <span data-ttu-id="180fb-128">Esse erro é basicamente causado devido à grafia incorreta da cadeia de caracteres ADsPath ao associar a um objeto.</span><span class="sxs-lookup"><span data-stu-id="180fb-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="180fb-129">Consulte [códigos de erro com genéricos](generic-com-error-codes.md) para obter mais alguns exemplos de erros com que podem ocorrer na programação ADSI.</span><span class="sxs-lookup"><span data-stu-id="180fb-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="180fb-130">Erros do Win32</span><span class="sxs-lookup"><span data-stu-id="180fb-130">Win32 Errors</span></span>

<span data-ttu-id="180fb-131">Qualquer código de erro do formato hexadecimal 8007xxxx é um código de erro Win32 padrão.</span><span class="sxs-lookup"><span data-stu-id="180fb-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="180fb-132">Se você converter os últimos quatro dígitos de hexadecimal para decimal, poderá acessar o erro na linha de comando do Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="180fb-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="180fb-133">**NET HELPMSG <number>**</span><span class="sxs-lookup"><span data-stu-id="180fb-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="180fb-134">Na linha de comando acima, " &lt; número &gt; " é o número decimal obtido pela conversão dos últimos quatro dígitos do código de erro de hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="180fb-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="180fb-135">Essa linha de comando fornecerá uma descrição mais útil do erro do Win32, que pode ser de grande ajuda para depurar seu script.</span><span class="sxs-lookup"><span data-stu-id="180fb-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





