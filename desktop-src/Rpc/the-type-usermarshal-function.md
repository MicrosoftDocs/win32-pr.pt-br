---
title: A função type_UserMarshal
description: A \_ função de Usermarshal do tipo é uma função auxiliar para os \_ atributos \ Wire Marshal e \ user \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366674"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="b5259-104">A \_ função de Usermarshal do tipo</span><span class="sxs-lookup"><span data-stu-id="b5259-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="b5259-105">A função **<type> \_ usermarshal** é uma função auxiliar para os \[ [atributos \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e \[ [ \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="b5259-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="b5259-106">Os stubs chamam essa função para realizar marshaling de dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="b5259-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="b5259-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="b5259-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="b5259-108">O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="b5259-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="b5259-109">Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — um tipo desconhecido para o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="b5259-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="b5259-110">O nome do tipo de fio (o nome do tipo Transmissible) não é usado no protótipo de função.</span><span class="sxs-lookup"><span data-stu-id="b5259-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="b5259-111">Observe, no entanto, que o tipo de conexão define o layout de fio para os dados, conforme especificado pelo uso DCE.</span><span class="sxs-lookup"><span data-stu-id="b5259-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="b5259-112">O parâmetro *pFlags* é um ponteiro para um campo de sinalizador longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="b5259-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="b5259-113">A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b5259-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="b5259-114">A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM.</span><span class="sxs-lookup"><span data-stu-id="b5259-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="b5259-115">O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5259-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="b5259-116">O parâmetro *pBuffer* é o ponteiro de buffer atual.</span><span class="sxs-lookup"><span data-stu-id="b5259-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="b5259-117">Esse ponteiro pode ou não estar alinhado na entrada.</span><span class="sxs-lookup"><span data-stu-id="b5259-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="b5259-118">Sua função **<type> \_ usermarshal** deve alinhar o ponteiro do buffer adequadamente, empacotar os dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto marshaled.</span><span class="sxs-lookup"><span data-stu-id="b5259-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="b5259-119">Tenha em mente que a especificação de tipo de conexão determina o layout real dos dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="b5259-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="b5259-120">O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="b5259-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="b5259-121">O valor de retorno é a nova posição do buffer, que é o endereço do primeiro byte após o objeto sem marshaling.</span><span class="sxs-lookup"><span data-stu-id="b5259-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="b5259-122">O estouro de buffer pode ocorrer quando você calcula incorretamente o tamanho dos dados e tenta realizar marshaling de mais dados do que o esperado.</span><span class="sxs-lookup"><span data-stu-id="b5259-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="b5259-123">Você deve ter cuidado para evitar essa situação.</span><span class="sxs-lookup"><span data-stu-id="b5259-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="b5259-124">Você pode verificar em relação a ele usando o ponteiro retornado pelo **<type> \_ usermarshal** .</span><span class="sxs-lookup"><span data-stu-id="b5259-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="b5259-125">Caso contrário, você correrá o risco de ter o mecanismo de NDR disparar uma exceção de estouro de buffer posteriormente.</span><span class="sxs-lookup"><span data-stu-id="b5259-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="b5259-126">As exceções devem ser capturadas e manipuladas localmente, as exceções não devem ter permissão para propigatedr a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="b5259-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5259-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5259-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5259-128">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="b5259-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b5259-129">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="b5259-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="b5259-130">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="b5259-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 