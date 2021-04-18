---
title: O atributo user_marshal
description: O atributo \ user \_ Marshal \ é um atributo de tipo ACF semelhante em sintaxe para \ representa \_ como \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, atributos user_marshal de chamada de procedimento remoto
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454237"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="114e5-105">O \_ atributo de marshaling do usuário</span><span class="sxs-lookup"><span data-stu-id="114e5-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="114e5-106">O \[ [atributo \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] é um atributo de tipo ACF semelhante na sintaxe para \[ [representar \_ como](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="114e5-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="114e5-107">Assim como acontece com o atributo IDL, o \[ [ \_ marshaling](/windows/desktop/Midl/wire-marshal) \] é uma maneira mais eficiente de empacotar dados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="114e5-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="114e5-108">Como um atributo ACF, o **\[ \_ marshaling \] do usuário** permite que você realize marshaling de tipos de dados personalizados que são desconhecidos para MIDL.</span><span class="sxs-lookup"><span data-stu-id="114e5-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="114e5-109">Cada tipo específico de aplicativo tem um tipo de transmissão correspondente que define a representação de transmissão.</span><span class="sxs-lookup"><span data-stu-id="114e5-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="114e5-110">O tipo específico do aplicativo pode ser um tipo simples, composto ou de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="114e5-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="114e5-111">A principal restrição é que a instância do tipo deve ter um tamanho de memória fixo e bem definido.</span><span class="sxs-lookup"><span data-stu-id="114e5-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="114e5-112">Se o tamanho da instância do tipo precisar ser alterado, use um campo de ponteiro em vez de uma matriz compatível.</span><span class="sxs-lookup"><span data-stu-id="114e5-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="114e5-113">Como alternativa, você pode definir um ponteiro para o tipo de alteração.</span><span class="sxs-lookup"><span data-stu-id="114e5-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="114e5-114">Assim como acontece com o atributo de **\[ \_ marshaling \] de fio** , você fornece rotinas para o dimensionamento, o marshaling, o desempacotamento e a liberação de passagens.</span><span class="sxs-lookup"><span data-stu-id="114e5-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="114e5-115">A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="114e5-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="114e5-116">O <type> é o *tipo* de usuário especificado na definição de tipo de **\[ \_ marshaling \] do usuário** .</span><span class="sxs-lookup"><span data-stu-id="114e5-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="114e5-117">Rotina</span><span class="sxs-lookup"><span data-stu-id="114e5-117">Routine</span></span>                                                            | <span data-ttu-id="114e5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="114e5-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="114e5-119"><type>\_Usersize</span><span class="sxs-lookup"><span data-stu-id="114e5-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="114e5-120">Dimensiona o buffer de dados RPC antes do marshaling no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="114e5-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="114e5-121"><type>\_Usermarshal</span><span class="sxs-lookup"><span data-stu-id="114e5-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="114e5-122">Realiza marshaling dos dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="114e5-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="114e5-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="114e5-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="114e5-124">Desempacota os dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="114e5-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="114e5-125"><type>\_Isfree</span><span class="sxs-lookup"><span data-stu-id="114e5-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="114e5-126">Libera os dados no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="114e5-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="114e5-127">Essas rotinas fornecidas pelo usuário são fornecidas pelo cliente ou pelo aplicativo de servidor, com base nos atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="114e5-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="114e5-128">Se o parâmetro for \[ [](/windows/desktop/Midl/in) \] somente, o cliente transmitirá para o servidor.</span><span class="sxs-lookup"><span data-stu-id="114e5-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="114e5-129">O cliente precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** .</span><span class="sxs-lookup"><span data-stu-id="114e5-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="114e5-130">O servidor precisa das funções **<type> \_ UserUnmarshal** e **<type> \_ userfree** .</span><span class="sxs-lookup"><span data-stu-id="114e5-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="114e5-131">Para um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out, o servidor transmite para o cliente.</span><span class="sxs-lookup"><span data-stu-id="114e5-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="114e5-132">O servidor precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** , enquanto o cliente precisa da função **<type> \_ usermarshal** .</span><span class="sxs-lookup"><span data-stu-id="114e5-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="114e5-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="114e5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="114e5-134">O \_ atributo de marshaling de fio</span><span class="sxs-lookup"><span data-stu-id="114e5-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="114e5-135">Regras de marshaling para marshaling de usuário e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="114e5-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="114e5-136">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="114e5-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="114e5-137">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="114e5-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="114e5-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="114e5-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 