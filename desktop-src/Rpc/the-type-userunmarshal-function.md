---
title: A função type_UserUnmarshal
description: A \_ função Type UserUnmarshal é uma função auxiliar para os atributos \ Wire \_ Marshal e \ user \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008323"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="36833-104">A \_ função Type UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="36833-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="36833-105">A função **<type> \_ UserUnmarshal** é uma função auxiliar para os atributos de marshaling de \[ [conexão \_](/windows/desktop/Midl/wire-marshal) \] e de \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="36833-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="36833-106">Os stubs chamam essa função para desempacotar dados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="36833-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="36833-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="36833-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="36833-108">O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="36833-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="36833-109">Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — desconhecido para o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="36833-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="36833-110">O nome do tipo de fio (o nome do tipo Transmissible) não é usado no protótipo de função.</span><span class="sxs-lookup"><span data-stu-id="36833-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="36833-111">Observe, no entanto, que o tipo de conexão define o layout de fio para os dados, conforme especificado pelo uso DCE.</span><span class="sxs-lookup"><span data-stu-id="36833-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="36833-112">O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** .</span><span class="sxs-lookup"><span data-stu-id="36833-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="36833-113">A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres.</span><span class="sxs-lookup"><span data-stu-id="36833-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="36833-114">A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM.</span><span class="sxs-lookup"><span data-stu-id="36833-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="36833-115">O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="36833-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="36833-116">O parâmetro *pBuffer* é o ponteiro de buffer atual.</span><span class="sxs-lookup"><span data-stu-id="36833-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="36833-117">Esse ponteiro pode ou não estar alinhado na entrada.</span><span class="sxs-lookup"><span data-stu-id="36833-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="36833-118">Sua função **<type> \_ UserUnmarshal** deve alinhar o ponteiro do buffer adequadamente, desempacotar os dados e retornar a nova posição do buffer, que é o endereço do primeiro byte após o objeto sem marshaling.</span><span class="sxs-lookup"><span data-stu-id="36833-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="36833-119">O parâmetro *pMyObj* é um ponteiro para um objeto de tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="36833-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="36833-120">Em um ambiente heterogêneo, o mecanismo de NDR executa qualquer conversão de dados necessária antes de chamar a função **<type> \_ UserUnmarshal** .</span><span class="sxs-lookup"><span data-stu-id="36833-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="36833-121">Observe que o mecanismo de NDR realiza essa conversão de dados de acordo com a definição de tipo de fio fornecida para esse tipo de dados de usuário.</span><span class="sxs-lookup"><span data-stu-id="36833-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="36833-122">O sinalizador indica a representação de dados do remetente.</span><span class="sxs-lookup"><span data-stu-id="36833-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36833-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36833-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36833-124">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="36833-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="36833-125">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="36833-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="36833-126">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="36833-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 