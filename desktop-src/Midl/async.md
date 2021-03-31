---
title: atributo Async
description: O atributo \ Async \ ACF define uma chamada de procedimento remoto como uma operação assíncrona.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL de atributo assíncrono
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917222"
---
# <a name="async-attribute"></a><span data-ttu-id="327e6-104">atributo Async</span><span class="sxs-lookup"><span data-stu-id="327e6-104">async attribute</span></span>

<span data-ttu-id="327e6-105">O \[  \] atributo Async ACF define uma chamada de procedimento remoto como uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="327e6-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="327e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="327e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327e6-107">*aceitar-ACF-atributos*</span><span class="sxs-lookup"><span data-stu-id="327e6-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="327e6-108">Especifica atributos de configuração de aplicativo opcionais.</span><span class="sxs-lookup"><span data-stu-id="327e6-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="327e6-109">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="327e6-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="327e6-110">Especifica o nome da função no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="327e6-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="327e6-111">*parâmetro-lista*</span><span class="sxs-lookup"><span data-stu-id="327e6-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="327e6-112">Especifica uma lista de parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="327e6-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="327e6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="327e6-113">Remarks</span></span>

<span data-ttu-id="327e6-114">Este atributo não é aplicável em interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="327e6-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="327e6-115">Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="327e6-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="327e6-116">Em seguida, modifique essa declaração de função, dentro do arquivo de configuração de aplicativo (ACF), aplicando o \[  \] atributo Async.</span><span class="sxs-lookup"><span data-stu-id="327e6-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="327e6-117">Observe que a declaração de função não faz menção do identificador assíncrono e que o identificador de associação é o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="327e6-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="327e6-118">A aplicação do \[ atributo **Async** \] no arquivo ACF gera o código apropriado para que, quando essa função for chamada, o servidor assíncrono Espere receber um identificador assíncrono antes dos outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="327e6-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="327e6-119">O atributo Async não pode ser usado com a opção de linha de comando [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="327e6-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="327e6-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="327e6-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="327e6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="327e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327e6-122">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="327e6-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="327e6-123">RPC assíncrono</span><span class="sxs-lookup"><span data-stu-id="327e6-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 