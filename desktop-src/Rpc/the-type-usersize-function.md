---
title: A função type_UserSize
description: A \_ função de Usersize do tipo é uma função auxiliar para os \_ atributos \ Wire Marshal e \ user \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641779"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="1ee0b-104">A \_ função de Usersize do tipo</span><span class="sxs-lookup"><span data-stu-id="1ee0b-104">The type\_UserSize Function</span></span>

<span data-ttu-id="1ee0b-105">A função **<type> \_ usersize** é uma função auxiliar para os \[ [atributos \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e \[ [ \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="1ee0b-106">Os stubs chamam essa função para dimensionar o buffer de dados RPC para o objeto de dados do usuário antes que os dados sejam empacotados no lado do cliente ou do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="1ee0b-107">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="1ee0b-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="1ee0b-108">O <type> no nome da função significa o tipo de usuário, conforme especificado na definição de tipo de marshaling de **\[ \_ \] fio** ou de marshaling de **\[ usuário \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="1ee0b-109">Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — desconhecido para o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="1ee0b-110">O nome do tipo de fio (o nome do tipo transmitido pela rede) não é usado no protótipo de função.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="1ee0b-111">Observe, no entanto, que o tipo de conexão define o layout dos dados, conforme especificado pelo uso DCE.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="1ee0b-112">Todos os dados devem ser convertidos no formato de NDR (representação de dados de rede).</span><span class="sxs-lookup"><span data-stu-id="1ee0b-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="1ee0b-113">O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="1ee0b-114">A palavra superior do sinalizador contém sinalizadores de formato NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="1ee0b-115">A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="1ee0b-116">O layout exato dos sinalizadores dentro do campo é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="1ee0b-117">Bits</span><span class="sxs-lookup"><span data-stu-id="1ee0b-117">Bits</span></span>  | <span data-ttu-id="1ee0b-118">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="1ee0b-118">Flag</span></span>                                  | <span data-ttu-id="1ee0b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee0b-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee0b-120">31-24</span><span class="sxs-lookup"><span data-stu-id="1ee0b-120">31-24</span></span> | <span data-ttu-id="1ee0b-121">Representação de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="1ee0b-121">Floating-point representation</span></span>         | <span data-ttu-id="1ee0b-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="1ee0b-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="1ee0b-123">23-20</span><span class="sxs-lookup"><span data-stu-id="1ee0b-123">23-20</span></span> | <span data-ttu-id="1ee0b-124">Ordem de byte de ponto flutuante e inteiro</span><span class="sxs-lookup"><span data-stu-id="1ee0b-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="1ee0b-125">0 = big-endian 1 = little-endian</span><span class="sxs-lookup"><span data-stu-id="1ee0b-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="1ee0b-126">19-16</span><span class="sxs-lookup"><span data-stu-id="1ee0b-126">19-16</span></span> | <span data-ttu-id="1ee0b-127">Representação de caracteres</span><span class="sxs-lookup"><span data-stu-id="1ee0b-127">Character representation</span></span>              | <span data-ttu-id="1ee0b-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="1ee0b-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="1ee0b-129">15-0</span><span class="sxs-lookup"><span data-stu-id="1ee0b-129">15-0</span></span>  | <span data-ttu-id="1ee0b-130">Sinalizador de contexto de marshaling</span><span class="sxs-lookup"><span data-stu-id="1ee0b-130">Marshaling context flag</span></span>               | <span data-ttu-id="1ee0b-131">0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc</span><span class="sxs-lookup"><span data-stu-id="1ee0b-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="1ee0b-132">O sinalizador de contexto de marshaling torna possível alterar o comportamento de sua rotina, dependendo do contexto da chamada RPC.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="1ee0b-133">Por exemplo, se você tiver um identificador (**longo**) para um bloco de dados, poderá enviar o identificador para uma chamada em processo, mas enviaria os dados reais para uma chamada para um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="1ee0b-134">O sinalizador de contexto de marshaling e seus valores são definidos nos arquivos wtypes. h e wtypes. idl no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="1ee0b-135">Quando o tipo de fio é definido corretamente, você não precisa usar os sinalizadores de formato NDR, pois o mecanismo de NDR executa as conversões necessárias.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="1ee0b-136">O *StartingSize* um parâmetro é o deslocamento do buffer atual.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="1ee0b-137">O tamanho inicial indica o deslocamento do buffer para o objeto de usuário e pode ou não estar alinhado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="1ee0b-138">Sua rotina deve considerar qualquer preenchimento necessário.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="1ee0b-139">O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="1ee0b-140">O valor de retorno é o novo deslocamento ou a posição do buffer.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="1ee0b-141">A função deve retornar o tamanho cumulativo, que é o tamanho inicial mais o preenchimento possível mais o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="1ee0b-142">A função **<type> \_ usersize** pode retornar um superestimar do tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="1ee0b-143">O tamanho real do buffer enviado é definido pelo tamanho dos dados, não pelo tamanho de alocação do buffer.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="1ee0b-144">A função **<type> \_ usersize** não será chamada se o tamanho da conexão puder ser calculado no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="1ee0b-145">Observe que, para a maioria das uniões, mesmo que não haja ponteiros, o tamanho real da representação de transmissão pode ser determinado somente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee0b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ee0b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee0b-147">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="1ee0b-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="1ee0b-148">Marshal do usuário \_</span><span class="sxs-lookup"><span data-stu-id="1ee0b-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="1ee0b-149">\_marshaling de transmissão</span><span class="sxs-lookup"><span data-stu-id="1ee0b-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 