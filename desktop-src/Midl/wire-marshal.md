---
title: Atributo wire_marshal
description: O atributo \ Wire \_ Marshal \ tem um tipo de dados que será usado para transmissão (o tipo de cabo) em vez de um tipo de dados específico do aplicativo (o tipo de usuário).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal do atributo MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366840"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="f0abb-104">\_atributo de marshaling de fio</span><span class="sxs-lookup"><span data-stu-id="f0abb-104">wire\_marshal attribute</span></span>

<span data-ttu-id="f0abb-105">O atributo de **\[ \_ marshaling \] de fio** especifica um tipo de dados que será usado para transmissão (o tipo de *cabo*) em vez de um tipo de dados específico do aplicativo (o *tipo de usuário*).</span><span class="sxs-lookup"><span data-stu-id="f0abb-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="f0abb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0abb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0abb-107">*tipo de fio*</span><span class="sxs-lookup"><span data-stu-id="f0abb-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-108">Especifica o tipo de dados de transferência nomeado que é realmente transferido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="f0abb-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="f0abb-109">O *tipo de conexão* deve ser um tipo base de MIDL, um tipo predefinido ou um identificador de tipo de um tipo que pode ser transmitido pela rede.</span><span class="sxs-lookup"><span data-stu-id="f0abb-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-110">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="f0abb-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-111">O tipo para o qual o *tipo de usuário* se tornará um alias.</span><span class="sxs-lookup"><span data-stu-id="f0abb-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-112">*tipo de usuário*</span><span class="sxs-lookup"><span data-stu-id="f0abb-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-113">Especifica o identificador do tipo de dados do usuário a ser empacotado.</span><span class="sxs-lookup"><span data-stu-id="f0abb-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="f0abb-114">Ele pode ser qualquer tipo, conforme fornecido pelo *especificador de tipo*, desde que tenha um tamanho bem definido.</span><span class="sxs-lookup"><span data-stu-id="f0abb-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="f0abb-115">O *tipo User-Type* não precisa ser transmititable, mas deve ser um tipo conhecido pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="f0abb-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-116">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="f0abb-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-117">Especifica um ponteiro para um campo de sinalizador ( [**longo**](long.md) [**sem sinal**](unsigned.md) ).</span><span class="sxs-lookup"><span data-stu-id="f0abb-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="f0abb-118">A palavra de ordem superior especifica sinalizadores de representação de dados de NDR, conforme definido pela DCE para ponto flutuante, Big ou little-endian e representação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0abb-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="f0abb-119">A palavra de ordem inferior Especifica um sinalizador de contexto de marshaling.</span><span class="sxs-lookup"><span data-stu-id="f0abb-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="f0abb-120">O layout exato dos sinalizadores é descrito na [ \_ função tipo usersize](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="f0abb-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-121">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="f0abb-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-122">Especifica o tamanho atual do buffer (deslocamento) antes de dimensionar o objeto.</span><span class="sxs-lookup"><span data-stu-id="f0abb-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-123">*tipo de pUser \_*</span><span class="sxs-lookup"><span data-stu-id="f0abb-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-124">Especifica um ponteiro para um objeto de *tipo de usuário \_ .*</span><span class="sxs-lookup"><span data-stu-id="f0abb-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="f0abb-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="f0abb-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f0abb-126">Especifica o ponteiro do buffer atual.</span><span class="sxs-lookup"><span data-stu-id="f0abb-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0abb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0abb-127">Remarks</span></span>

<span data-ttu-id="f0abb-128">Cada tipo de dados específico do aplicativo, *tipo de usuário,* tem uma correspondência um-para-um com um *tipo de conexão* que define a representação de transmissão do tipo.</span><span class="sxs-lookup"><span data-stu-id="f0abb-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="f0abb-129">Você deve fornecer rotinas para dimensionar os dados para marshaling, para realizar marshaling e desempacotamento dos dados e para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="f0abb-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="f0abb-130">Observe que, se houver tipos inseridos em seus dados que também são definidos com marshaling de **\[ conexão \_ \]** ou **\[** [**\_ marshaling do usuário**](user-marshal.md) **\]** , você precisará gerenciar a manutenção desses tipos inseridos também.</span><span class="sxs-lookup"><span data-stu-id="f0abb-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="f0abb-131">Para obter mais informações sobre essas rotinas, consulte [o \_ atributo de marshaling de fio](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="f0abb-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="f0abb-132">Sua implementação deve seguir as regras de Marshalling de acordo com a especificação uso-DCE.</span><span class="sxs-lookup"><span data-stu-id="f0abb-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="f0abb-133">Detalhes sobre a sintaxe de transferência de NDR podem ser encontrados em [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) .</span><span class="sxs-lookup"><span data-stu-id="f0abb-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="f0abb-134">Não é recomendável usar o **\[ \_ marshaling \] de conexão** se você não estiver familiarizado com o protocolo de conexão.</span><span class="sxs-lookup"><span data-stu-id="f0abb-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="f0abb-135">O *tipo de conexão* não pode ser um ponteiro de interface nem um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="f0abb-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="f0abb-136">O *tipo de conexão* deve ter um tamanho de memória bem definido.</span><span class="sxs-lookup"><span data-stu-id="f0abb-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="f0abb-137">Consulte marshaling [Rules for User Marshal \_ and wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para obter detalhes sobre como realizar marshaling de um determinado *tipo de cabo*.</span><span class="sxs-lookup"><span data-stu-id="f0abb-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="f0abb-138">O *tipo de usuário* não deve ser um ponteiro de interface porque pode ser empacotado diretamente.</span><span class="sxs-lookup"><span data-stu-id="f0abb-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="f0abb-139">Se o tipo de usuário for um ponteiro completo, você mesmo precisará gerenciar o alias.</span><span class="sxs-lookup"><span data-stu-id="f0abb-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="f0abb-140">Você não pode usar o atributo de **\[ \_ marshaling \] de fio** com o **\[** [](allocate.md) **\]** atributo Allocate, direta ou indiretamente, porque o mecanismo de NDR não controla a alocação de memória para o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="f0abb-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="f0abb-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0abb-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="f0abb-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0abb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0abb-143">**aloca**</span><span class="sxs-lookup"><span data-stu-id="f0abb-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="f0abb-144">Representação de dados</span><span class="sxs-lookup"><span data-stu-id="f0abb-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="f0abb-145">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="f0abb-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f0abb-146">**Longas**</span><span class="sxs-lookup"><span data-stu-id="f0abb-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="f0abb-147">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="f0abb-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="f0abb-148">O \_ atributo de marshaling de fio</span><span class="sxs-lookup"><span data-stu-id="f0abb-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="f0abb-149">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="f0abb-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="f0abb-150">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="f0abb-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="f0abb-151">**Marshal do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="f0abb-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 