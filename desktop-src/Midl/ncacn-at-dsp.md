---
title: ncacn_at_dsp atributo
description: A \_ \_ palavra-chave ncacn at DSP identifica o DSP do AppleTalk como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917266"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="97034-105">ncacn \_ no \_ atributo DSP</span><span class="sxs-lookup"><span data-stu-id="97034-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="97034-106">A palavra-chave **ncacn \_ at \_ DSP** identifica o DSP do AppleTalk como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="97034-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="97034-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="97034-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="97034-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97034-109">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="97034-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="97034-110">Especifica uma cadeia de caracteres de até 22 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="97034-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97034-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="97034-111">Remarks</span></span>

<span data-ttu-id="97034-112">A sintaxe da cadeia de caracteres de porta do DSP do AppleTalk, como todas as cadeias de porta, é definida pela implementação do transporte e é independente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="97034-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="97034-113">O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="97034-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="97034-114">Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="97034-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="97034-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97034-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="97034-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="97034-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97034-117">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="97034-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="97034-118">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="97034-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="97034-119">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="97034-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 