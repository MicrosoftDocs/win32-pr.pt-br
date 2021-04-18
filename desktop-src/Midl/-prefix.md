---
title: comutador/prefix
description: A opção/prefix instrui o compilador MIDL a adicionar cadeias de caracteres de prefixo aos nomes de rotina de stub do cliente e/ou servidor.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL do comutador/prefix
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104498899"
---
# <a name="prefix-switch"></a><span data-ttu-id="4f909-104">comutador/prefix</span><span class="sxs-lookup"><span data-stu-id="4f909-104">/prefix switch</span></span>

<span data-ttu-id="4f909-105">A opção **/prefix** instrui o compilador MIDL a adicionar cadeias de caracteres de prefixo aos nomes de rotina de stub do cliente e/ou servidor.</span><span class="sxs-lookup"><span data-stu-id="4f909-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="4f909-106">Isso pode ser usado para permitir que um único programa seja um cliente e um servidor da mesma interface, sem que os nomes de rotina do cliente e do servidor entrem em conflito entre si.</span><span class="sxs-lookup"><span data-stu-id="4f909-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="4f909-107">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="4f909-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="4f909-108"><span id="client"></span><span id="CLIENT"></span>cliente \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4f909-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-109">Afeta apenas os nomes de rotina de stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f909-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="4f909-110"><span id="cstub"></span><span id="CSTUB"></span>cstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f909-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-111">Igual ao *cliente*.</span><span class="sxs-lookup"><span data-stu-id="4f909-111">Same as *client*.</span></span> <span data-ttu-id="4f909-112">Afeta apenas os nomes de rotina de stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f909-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="4f909-113"><span id="server"></span><span id="SERVER"></span>servidor \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4f909-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-114">Afeta apenas os nomes de rotina chamados pela rotina de stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="4f909-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="4f909-115"><span id="sstub"></span><span id="SSTUB"></span>sstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f909-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-116">Igual ao *servidor*.</span><span class="sxs-lookup"><span data-stu-id="4f909-116">Same as *server*.</span></span> <span data-ttu-id="4f909-117">Afeta apenas os nomes de rotina chamados pela rotina de stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="4f909-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="4f909-118"><span id="switch"></span><span id="SWITCH"></span>alternar \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4f909-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-119">Afeta um protótipo extra adicionado ao arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4f909-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="4f909-120"><span id="all"></span><span id="ALL"></span>todos \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4f909-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4f909-121">Afeta os nomes de rotina de stub do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="4f909-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f909-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f909-122">Remarks</span></span>

<span data-ttu-id="4f909-123">Se o prefixo das rotinas do lado do cliente for diferente do prefixo das rotinas do lado do servidor, o arquivo de cabeçalho gerado terá protótipos de rotina do lado do cliente e protótipos de rotina do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4f909-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="4f909-124">A opção **/prefix** é útil quando um único arquivo de cabeçalho for usado com stubs de várias execuções do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="4f909-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="4f909-125">Isso força protótipos de rotina adicionais no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="4f909-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="4f909-126">Em todos os casos, o cliente, o servidor e os prefixos de comutador substituirão um prefixo ALL.</span><span class="sxs-lookup"><span data-stu-id="4f909-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="4f909-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f909-127">Examples</span></span>

<span data-ttu-id="4f909-128">**MIDL/prefix cliente "c \_ " Server "s \_ "**</span><span class="sxs-lookup"><span data-stu-id="4f909-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="4f909-129">**MIDL/prefix All "Moo \_ "**</span><span class="sxs-lookup"><span data-stu-id="4f909-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="4f909-130">**cliente de MIDL/prefix "latido \_ "**</span><span class="sxs-lookup"><span data-stu-id="4f909-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="4f909-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f909-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f909-132">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="4f909-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




