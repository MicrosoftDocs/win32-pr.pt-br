---
title: O atributo wire_marshal
description: O atributo \ Wire \_ Marshal \ é um atributo de tipo IDL semelhante à sintaxe para \ transmitir \_ como \, mas fornecendo uma maneira mais eficiente de realizar marshaling de dados em uma rede.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, atributos wire_marshal de chamada de procedimento remoto
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366409"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="0640e-105">O \_ atributo de marshaling de fio</span><span class="sxs-lookup"><span data-stu-id="0640e-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="0640e-106">O \[ atributo de [ \_ marshaling de fio](/windows/desktop/Midl/wire-marshal) \] é um atributo de tipo IDL semelhante à sintaxe para \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] , mas fornecendo uma maneira mais eficiente de realizar marshaling de dados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="0640e-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="0640e-107">Use o atributo de \[ **\_ marshaling de fio** \] para especificar um tipo de dados que será transmitido no lugar do tipo de dados específico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0640e-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="0640e-108">Cada tipo específico de aplicativo tem um tipo de transmissão correspondente que define a representação de transmissão (a representação usada na rede). O tipo específico do aplicativo não precisa ser transmititable, mas deve ser um tipo que o MIDL reconhece.</span><span class="sxs-lookup"><span data-stu-id="0640e-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="0640e-109">Para empacotar um tipo desconhecido para MIDL, use o \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal)do atributo ACF \] .</span><span class="sxs-lookup"><span data-stu-id="0640e-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="0640e-110">O tipo específico do aplicativo pode ser um tipo simples, composto ou de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="0640e-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="0640e-111">A principal restrição é que a instância do tipo deve ter um tamanho de memória fixo e bem definido.</span><span class="sxs-lookup"><span data-stu-id="0640e-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="0640e-112">Se o tamanho da instância do tipo precisar ser alterado, use um campo de ponteiro em vez de uma matriz compatível.</span><span class="sxs-lookup"><span data-stu-id="0640e-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="0640e-113">Como alternativa, você pode definir um ponteiro para o tipo de alteração.</span><span class="sxs-lookup"><span data-stu-id="0640e-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="0640e-114">Você deve fornecer as rotinas para o dimensionamento, o marshaling e o desempacotamento dos dados, bem como a liberação da memória associada.</span><span class="sxs-lookup"><span data-stu-id="0640e-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="0640e-115">A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0640e-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="0640e-116">O <type> é o tipo de usuário especificado na definição do \[ tipo de **\_ marshaling de fio** \] .</span><span class="sxs-lookup"><span data-stu-id="0640e-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="0640e-117">Rotina</span><span class="sxs-lookup"><span data-stu-id="0640e-117">Routine</span></span>                                                            | <span data-ttu-id="0640e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0640e-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="0640e-119"><type>\_Usersize</span><span class="sxs-lookup"><span data-stu-id="0640e-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="0640e-120">Dimensiona o buffer de dados RPC antes do marshaling no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="0640e-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="0640e-121"><type>\_Usermarshal</span><span class="sxs-lookup"><span data-stu-id="0640e-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="0640e-122">Realiza marshaling dos dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="0640e-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="0640e-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="0640e-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="0640e-124">Desempacota os dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="0640e-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="0640e-125"><type>\_Isfree</span><span class="sxs-lookup"><span data-stu-id="0640e-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="0640e-126">Libera os dados no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="0640e-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="0640e-127">Essas rotinas fornecidas pelo programador são fornecidas pelo cliente ou pelo aplicativo de servidor com base nos atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="0640e-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="0640e-128">Se o parâmetro for \[ [](/windows/desktop/Midl/in) \] somente, o cliente transmitirá para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0640e-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="0640e-129">O cliente precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** .</span><span class="sxs-lookup"><span data-stu-id="0640e-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="0640e-130">O servidor precisa das funções **<type> \_ UserUnmarshal** e **<type> \_ userfree** .</span><span class="sxs-lookup"><span data-stu-id="0640e-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="0640e-131">Para um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out, o servidor transmite para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0640e-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="0640e-132">O servidor precisa das funções **<type> \_ usersize** e **<type> \_ usermarshal** , enquanto o cliente precisa da função **<type> \_ usermarshal** .</span><span class="sxs-lookup"><span data-stu-id="0640e-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0640e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0640e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0640e-134">O \_ atributo de marshaling do usuário</span><span class="sxs-lookup"><span data-stu-id="0640e-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="0640e-135">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="0640e-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="0640e-136">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="0640e-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="0640e-137">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="0640e-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="0640e-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="0640e-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 