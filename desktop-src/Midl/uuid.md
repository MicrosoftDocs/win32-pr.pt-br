---
title: atributo uuid
description: O atributo \ UUID \ interface designa um UUID (identificador universal exclusivo) que é atribuído à interface e que o distingue de outras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- MIDL de atributo uuid
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638580"
---
# <a name="uuid-attribute"></a><span data-ttu-id="a6ed7-104">atributo uuid</span><span class="sxs-lookup"><span data-stu-id="a6ed7-104">uuid attribute</span></span>

<span data-ttu-id="a6ed7-105">O atributo interface **\[ UUID \]** designa um UUID (identificador universal exclusivo) que é atribuído à interface e que o distingue de outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="a6ed7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6ed7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ed7-107">*Cadeia de caracteres-UUID*</span><span class="sxs-lookup"><span data-stu-id="a6ed7-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed7-108">Especifica uma cadeia de caracteres que consiste em 8 dígitos hexadecimais seguidos por um hífen, em seguida, três grupos de quatro dígitos hexadecimais, cada um seguido por um hífen e 12 dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="a6ed7-109">Você pode colocar a cadeia de caracteres UUID entre aspas, exceto quando você usar o [**/OSF**](-osf.md)do compilador MIDL switch.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ed7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6ed7-110">Remarks</span></span>

<span data-ttu-id="a6ed7-111">A biblioteca de tempo de execução usa o UUID de interface que o atributo **\[ UUID \]** designa para ajudar a estabelecer a comunicação entre os aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="a6ed7-112">O atributo **\[ UUID \]** pode aparecer na lista de atributos de interface para uma interface RPC ou uma interface com.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="a6ed7-113">Para uma interface RPC, a lista de atributos de interface deve incluir o atributo **\[ UUID \]** ou o **\[** [](local.md) **\]** atributo local, e aquele que você escolher deve ocorrer exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="a6ed7-114">Se a lista incluir o atributo **\[ UUID \]** , ela também poderá incluir o **\[** atributo [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a6ed7-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="a6ed7-115">Para uma interface COM (identificada pelo **\[** atributo de interface de [**objeto**](object.md) **\]** ), a lista de atributos de interface deve incluir o atributo **\[ UUID \]** , mas não pode incluir o atributo **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="a6ed7-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="a6ed7-116">A lista de uma interface COM pode incluir o atributo **\[ local \]** , embora o atributo **\[ UUID \]** esteja presente.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="a6ed7-117">O Microsoft RPC dá suporte a uma extensão para o DCE IDL que permite que o UUID seja colocado entre aspas duplas ("" "").</span><span class="sxs-lookup"><span data-stu-id="a6ed7-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="a6ed7-118">O formulário entre aspas é necessário para os pré-processadores do compilador C que interpretam números UUID como números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="a6ed7-119">Todos os valores UUID devem ser gerados por computador para garantir a exclusividade.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="a6ed7-120">Use o utilitário Uuidgen para gerar valores exclusivos de UUID.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="a6ed7-121">O UUID e os números de versão da interface são usados para determinar se o cliente pode se associar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="a6ed7-122">Para que o cliente seja associado ao servidor, o UUID especificado nas interfaces do cliente e do servidor deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="a6ed7-123">Observe que uma interface sem atributos pode ser importada para um arquivo IDL base.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="a6ed7-124">No entanto, a interface deve conter apenas tipos de texto sem procedimentos.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="a6ed7-125">Se até um procedimento estiver contido na interface, um atributo local ou UUID deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="a6ed7-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6ed7-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="a6ed7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6ed7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ed7-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a6ed7-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a6ed7-129">**interface**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="a6ed7-130">**local**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a6ed7-131">**objeto**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="a6ed7-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="a6ed7-133">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




