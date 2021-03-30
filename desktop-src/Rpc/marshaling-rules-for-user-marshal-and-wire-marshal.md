---
title: Regras de marshaling para user_marshal e wire_marshal
description: A especificação uso-DCE para empacotamento de tipos de ponteiros inseridos requer que você observe as seguintes restrições ao implementar o tipo \_ usersize, digite \_ usermarshal e digite \_ funções UserUnMarshal.
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641489"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="6ac96-103">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="6ac96-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="6ac96-104">A especificação uso-DCE para empacotamento de tipos de ponteiros inseridos requer que você observe as seguintes restrições ao implementar as <type> \_ funções usersize, <type> \_ usermarshal e <type> \_ UserUnMarshal.</span><span class="sxs-lookup"><span data-stu-id="6ac96-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="6ac96-105">(As regras e os exemplos fornecidos aqui são para o marshaling.</span><span class="sxs-lookup"><span data-stu-id="6ac96-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="6ac96-106">No entanto, suas rotinas de dimensionamento e desempacotamento devem seguir as mesmas restrições):</span><span class="sxs-lookup"><span data-stu-id="6ac96-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="6ac96-107">Se o tipo de fio for um tipo simples sem ponteiros, sua rotina de marshaling para o tipo de usuário correspondente deve simplesmente empacotar os dados de acordo com o layout do tipo de cabo.</span><span class="sxs-lookup"><span data-stu-id="6ac96-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="6ac96-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6ac96-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="6ac96-109">Observe que o tipo de fio, **Long**, é um tipo simples.</span><span class="sxs-lookup"><span data-stu-id="6ac96-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="6ac96-110">A função do manipulador de identificadores do \_ \_ usermarshal realiza um **longo tempo** sempre que um objeto identificador de identificador \_ é passado para ele.</span><span class="sxs-lookup"><span data-stu-id="6ac96-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="6ac96-111">Se o tipo de fio for um ponteiro para outro tipo, sua rotina de marshaling para o tipo de usuário correspondente deverá empacotar os dados de acordo com o layout do tipo ao qual o tipo de fio aponta.</span><span class="sxs-lookup"><span data-stu-id="6ac96-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="6ac96-112">O mecanismo de NDR cuida do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6ac96-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="6ac96-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6ac96-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="6ac96-114">Observe que o tipo de fio **, \_ tipo de fio**, é um tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6ac96-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="6ac96-115">A \_ função de Usermarshal de dados de manipulador \_ realiza marshaling dos dados relacionados ao identificador, usando o layout HDATA, em vez do \* layout HDATA.</span><span class="sxs-lookup"><span data-stu-id="6ac96-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="6ac96-116">Um tipo de fio deve ser um tipo de dados simples ou um tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6ac96-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="6ac96-117">Se seu tipo Transmissible deve ser algo diferente (uma estrutura com ponteiros, por exemplo), use um ponteiro para o tipo desejado como o tipo de cabo.</span><span class="sxs-lookup"><span data-stu-id="6ac96-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="6ac96-118">O efeito dessas restrições é que os tipos definidos com os atributos \[ [**\_ empacotamento de fio**](/windows/desktop/Midl/wire-marshal) \] ou \[ [**\_ marshaling do usuário**](/windows/desktop/Midl/user-marshal) \] podem ser inseridos livremente em outros tipos.</span><span class="sxs-lookup"><span data-stu-id="6ac96-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ac96-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ac96-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ac96-120">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="6ac96-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="6ac96-121">**Marshal do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="6ac96-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="6ac96-122">A \_ função de Usersize do tipo</span><span class="sxs-lookup"><span data-stu-id="6ac96-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="6ac96-123">A \_ função de Usermarshal do tipo</span><span class="sxs-lookup"><span data-stu-id="6ac96-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="6ac96-124">O tipo \_ UserUnMarshalFunction</span><span class="sxs-lookup"><span data-stu-id="6ac96-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="6ac96-125">O tipo \_ UserFreeFunction</span><span class="sxs-lookup"><span data-stu-id="6ac96-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 