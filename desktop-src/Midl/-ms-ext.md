---
title: opção/ms_ext
description: Em vigor com a versão 3,0 do MIDL, os recursos habilitados pela \_ opção MS ext agora são o modo padrão para o compilador MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext MIDL do comutador
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007404"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="f6ad3-104">\_comutador/MS ext</span><span class="sxs-lookup"><span data-stu-id="f6ad3-104">/ms\_ext switch</span></span>

<span data-ttu-id="f6ad3-105">Em vigor com a versão 3,0 do MIDL, os recursos habilitados pela opção **MS \_ ext** agora são o modo padrão para o compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="f6ad3-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="f6ad3-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="f6ad3-106">Switch Options</span></span>

<span data-ttu-id="f6ad3-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6ad3-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ad3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6ad3-108">Remarks</span></span>

<span data-ttu-id="f6ad3-109">Usar a opção não gerará um erro do compilador, portanto, você não precisa remover referências a **/MS \_ ext** ou [**/c \_ ext**](-c-ext.md) de um makefile existente.</span><span class="sxs-lookup"><span data-stu-id="f6ad3-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="f6ad3-110">As seguintes extensões da Microsoft para uso o DCE agora estão disponíveis por padrão:</span><span class="sxs-lookup"><span data-stu-id="f6ad3-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="f6ad3-111">Definições de interface para objetos OLE.</span><span class="sxs-lookup"><span data-stu-id="f6ad3-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="f6ad3-112">Para obter mais informações sobre os arquivos gerados para interfaces OLE, consulte [arquivos gerados para uma interface com](files-generated-for-a-com-interface.md)</span><span class="sxs-lookup"><span data-stu-id="f6ad3-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="f6ad3-113">Um atributo de [**\[ retorno de chamada \]**](callback.md) que especifica uma função de retorno de chamada estática no cliente</span><span class="sxs-lookup"><span data-stu-id="f6ad3-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="f6ad3-114">[**\_ aspas de CPP**](cpp-quote.md)(*cadeia de \_ caracteres entre aspas*) e [**\# \_ eco de MIDL de pragma**](pragma.md)</span><span class="sxs-lookup"><span data-stu-id="f6ad3-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="f6ad3-115">[**WCHAR \_ t**](wchar-t.md) largo-tipos de caractere, constantes e cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="f6ad3-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="f6ad3-116">[**inicialização de enumeração**](enum.md) (enumeradores esparsos)</span><span class="sxs-lookup"><span data-stu-id="f6ad3-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="f6ad3-117">Expressões como tamanho e especificadores de discriminador</span><span class="sxs-lookup"><span data-stu-id="f6ad3-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="f6ad3-118">Manipular extensões</span><span class="sxs-lookup"><span data-stu-id="f6ad3-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="f6ad3-119">Herança de tipo de atributo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f6ad3-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="f6ad3-120">Várias interfaces</span><span class="sxs-lookup"><span data-stu-id="f6ad3-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="f6ad3-121">Definições fora do bloco de interface</span><span class="sxs-lookup"><span data-stu-id="f6ad3-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="f6ad3-122">Você pode omitir os [atributos direcionais](/windows/desktop/Rpc/directional-parameter-attributes) para \[ [**dentro**](in.md), [**fora**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="f6ad3-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="f6ad3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6ad3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ad3-124">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="f6ad3-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f6ad3-125">Herança de tipo de atributo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f6ad3-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="f6ad3-126">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="f6ad3-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="f6ad3-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="f6ad3-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 