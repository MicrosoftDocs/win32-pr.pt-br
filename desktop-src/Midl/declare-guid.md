---
title: Palavra-chave declare_guid
description: A \_ palavra-chave declare GUID instrui o MIDL a emitir uma variável GUID para o arquivo de cabeçalho gerado.
keywords:
- MIDL de palavra-chave declare_guid
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105764347"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="a17bf-104">\_palavra-chave de GUID declare</span><span class="sxs-lookup"><span data-stu-id="a17bf-104">declare\_guid keyword</span></span>

<span data-ttu-id="a17bf-105">A palavra-chave **Declare \_ GUID** instrui o MIDL a emitir uma variável GUID para o arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="a17bf-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="a17bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a17bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a17bf-107">*nome da variável*</span><span class="sxs-lookup"><span data-stu-id="a17bf-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a17bf-108">Especifica um nome de variável para o identificador no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="a17bf-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="a17bf-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="a17bf-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="a17bf-110">Especifica o [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) que será aplicado ao nome da variável no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="a17bf-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a17bf-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a17bf-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="a17bf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a17bf-112">Remarks</span></span>

<span data-ttu-id="a17bf-113">O uso `declare_guid` do é equivalente ao uso `cpp_quote` do para gerar uma invocação da `EXTERN_GUID` macro.</span><span class="sxs-lookup"><span data-stu-id="a17bf-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="a17bf-114">O exemplo acima resulta na seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="a17bf-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="a17bf-115">A `declare_guid` instrução é fornecida como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="a17bf-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="a17bf-116">Ele tem a vantagem de usar a mesma sintaxe de GUID que o [ `uuid` atributo](uuid.md).</span><span class="sxs-lookup"><span data-stu-id="a17bf-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a17bf-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a17bf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17bf-118">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a17bf-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a17bf-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="a17bf-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="a17bf-120">**atributo uuid**</span><span class="sxs-lookup"><span data-stu-id="a17bf-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="a17bf-121">**Estrutura de GUID**</span><span class="sxs-lookup"><span data-stu-id="a17bf-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
