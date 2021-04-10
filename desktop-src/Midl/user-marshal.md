---
title: user_marshal atributo
description: O atributo de ACF do Marshal do usuário \_ associa um tipo de local nomeado no idioma de destino (tipo de usuário) a um tipo de transferência (tipo de fio) que é transferido entre o cliente e o servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal do atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293947"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="ac83f-104">\_atributo de marshaling do usuário</span><span class="sxs-lookup"><span data-stu-id="ac83f-104">user\_marshal attribute</span></span>

<span data-ttu-id="ac83f-105">O atributo de ACF do **\_ Marshal do usuário** associa um tipo de local nomeado no idioma de destino (*tipo de usuário*) a um tipo de transferência (*tipo de fio*) que é transferido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ac83f-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="ac83f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac83f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac83f-107">*tipo de usuário*</span><span class="sxs-lookup"><span data-stu-id="ac83f-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-108">Especifica o identificador do tipo de dados do usuário a ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="ac83f-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="ac83f-109">O *tipo User-Type* não precisa ser transmititable e não precisa ser um tipo conhecido pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="ac83f-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="ac83f-110">*tipo de fio*</span><span class="sxs-lookup"><span data-stu-id="ac83f-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-111">Especifica o tipo de dados de transferência nomeado que é realmente transferido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ac83f-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="ac83f-112">O tipo de conexão deve ser um tipo base de MIDL, um tipo predefinido ou um identificador de tipo de um tipo que pode ser transmitido pela rede.</span><span class="sxs-lookup"><span data-stu-id="ac83f-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="ac83f-113">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="ac83f-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-114">Especifica um ponteiro para um campo de sinalizador ( [**longo**](long.md) [**sem sinal**](unsigned.md) ).</span><span class="sxs-lookup"><span data-stu-id="ac83f-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="ac83f-115">A palavra de ordem superior especifica sinalizadores de representação de dados de NDR, conforme definido pela DCE para ponto flutuante, Big ou little-endian e representação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ac83f-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="ac83f-116">A palavra de ordem inferior Especifica um sinalizador de contexto de marshaling.</span><span class="sxs-lookup"><span data-stu-id="ac83f-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="ac83f-117">O layout exato dos sinalizadores é descrito na [ \_ função tipo usersize](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="ac83f-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="ac83f-118">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="ac83f-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-119">Especifica o tamanho atual do buffer (deslocamento) antes de dimensionar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ac83f-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="ac83f-120">*tipo de pUser \_*</span><span class="sxs-lookup"><span data-stu-id="ac83f-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-121">Especifica um ponteiro para um objeto de *\_ tipo de usuário*.</span><span class="sxs-lookup"><span data-stu-id="ac83f-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="ac83f-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="ac83f-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ac83f-123">Especifica o ponteiro do buffer atual.</span><span class="sxs-lookup"><span data-stu-id="ac83f-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac83f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac83f-124">Remarks</span></span>

<span data-ttu-id="ac83f-125">Cada tipo de local nomeado, *User-Type*, tem uma correspondência um-para-um com um *tipo de conexão* que define a representação de transmissão do tipo.</span><span class="sxs-lookup"><span data-stu-id="ac83f-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="ac83f-126">Você deve fornecer rotinas para dimensionar os dados para marshaling, para realizar marshaling e desempacotamento dos dados e para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="ac83f-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="ac83f-127">Para obter mais informações sobre essas rotinas, consulte [o \_ atributo Marshal do usuário](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="ac83f-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="ac83f-128">Observe que, se houver tipos inseridos em seus dados que também são definidos com marshaling do **usuário \_** ou \[ [**\[ \_ \] marshaling de conexão**](wire-marshal.md), você precisará gerenciar a manutenção desses tipos inseridos também.</span><span class="sxs-lookup"><span data-stu-id="ac83f-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="ac83f-129">O *tipo de conexão* não pode ser um ponteiro de interface nem um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="ac83f-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="ac83f-130">O *tipo de conexão* deve ter um tamanho de memória bem definido.</span><span class="sxs-lookup"><span data-stu-id="ac83f-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="ac83f-131">Consulte marshaling [Rules for User Marshal \_ and wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para obter detalhes sobre como realizar marshaling de um determinado *tipo de cabo*.</span><span class="sxs-lookup"><span data-stu-id="ac83f-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="ac83f-132">O *tipo de usuário* não deve ser um ponteiro de interface, pois eles podem ser empacotados diretamente.</span><span class="sxs-lookup"><span data-stu-id="ac83f-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="ac83f-133">Se o tipo de usuário for um ponteiro completo, você mesmo precisará gerenciar o alias.</span><span class="sxs-lookup"><span data-stu-id="ac83f-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="ac83f-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac83f-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="ac83f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac83f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac83f-136">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="ac83f-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ac83f-137">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="ac83f-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ac83f-138">**Longas**</span><span class="sxs-lookup"><span data-stu-id="ac83f-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="ac83f-139">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="ac83f-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="ac83f-140">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="ac83f-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="ac83f-141">O \_ atributo de marshaling do usuário</span><span class="sxs-lookup"><span data-stu-id="ac83f-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="ac83f-142">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="ac83f-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="ac83f-143">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="ac83f-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 