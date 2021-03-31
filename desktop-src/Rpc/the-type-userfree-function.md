---
title: A função type_UserFree
description: O tipo \_ função de usuário livre é uma função auxiliar para os atributos \ Wire \_ Marshal \ e \ user \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641135"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="3be07-104">O tipo \_ função Userfree</span><span class="sxs-lookup"><span data-stu-id="3be07-104">The type\_UserFree Function</span></span>

<span data-ttu-id="3be07-105">A função **<type> \_ userfree** é uma função auxiliar para os \[ atributos de [ \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e de \[ [ \_ marshaling do usuário](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="3be07-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="3be07-106">Os stubs chamam essa função para liberar os dados no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="3be07-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="3be07-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="3be07-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="3be07-108">O <type> no nome da função significa o tipo de usuário especificado na definição de tipo de marshaling de **\[ \_ \] conexão** ou de **\[ usuário \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="3be07-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="3be07-109">O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** .</span><span class="sxs-lookup"><span data-stu-id="3be07-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="3be07-110">A palavra superior do sinalizador contém sinalizadores de representação de dados de NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3be07-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="3be07-111">A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM.</span><span class="sxs-lookup"><span data-stu-id="3be07-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="3be07-112">O layout exato dos sinalizadores dentro do campo é descrito na [função do tipo \_ usersize](the-type-usersize-function.md).</span><span class="sxs-lookup"><span data-stu-id="3be07-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="3be07-113">O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="3be07-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="3be07-114">O mecanismo de NDR libera o objeto de nível superior.</span><span class="sxs-lookup"><span data-stu-id="3be07-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="3be07-115">Você é responsável por liberar todos os objetos aos quais o objeto de nível superior pode apontar.</span><span class="sxs-lookup"><span data-stu-id="3be07-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="3be07-116">As exceções devem ser capturadas e manipuladas localmente, as exceções não devem ter permissão para propigatedr a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="3be07-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3be07-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3be07-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be07-118">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="3be07-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="3be07-119">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="3be07-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="3be07-120">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="3be07-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 