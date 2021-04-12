---
title: opção/app_config
description: A \_ opção/app config seleciona o modo de configuração de aplicativo, que permite que você use algumas palavras-chave ACF no arquivo IDL. Com essa opção de compilador MIDL, você pode omitir o ACF e especificar uma interface em um único arquivo IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config MIDL do comutador
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364953"
---
# <a name="app_config-switch"></a><span data-ttu-id="1f493-105">\_opção de configuração/app</span><span class="sxs-lookup"><span data-stu-id="1f493-105">/app\_config switch</span></span>

<span data-ttu-id="1f493-106">A opção **/app \_ config** seleciona o modo de configuração de aplicativo, que permite que você use algumas palavras-chave ACF no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1f493-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="1f493-107">Com essa opção de compilador MIDL, você pode omitir o ACF e especificar uma interface em um único arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1f493-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="1f493-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="1f493-108">Switch Options</span></span>

<span data-ttu-id="1f493-109">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1f493-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f493-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f493-110">Remarks</span></span>

<span data-ttu-id="1f493-111">O Microsoft RPC dá suporte ao uso dos seguintes atributos de ACF no arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="1f493-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="1f493-112">\_Identificador implícito</span><span class="sxs-lookup"><span data-stu-id="1f493-112">Implicit\_handle</span></span>
-   <span data-ttu-id="1f493-113">\_Identificador automático</span><span class="sxs-lookup"><span data-stu-id="1f493-113">Auto\_handle</span></span>
-   <span data-ttu-id="1f493-114">\_Identificador explícito</span><span class="sxs-lookup"><span data-stu-id="1f493-114">Explicit\_handle</span></span>

<span data-ttu-id="1f493-115">Versões futuras do Microsoft RPC podem dar suporte ao uso de outros atributos de ACF no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1f493-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="1f493-116">A opção de **\_ configuração/app** representa uma extensão da Microsoft para a especificação uso-DCE e, como tal, é mutuamente exclusiva com a opção [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="1f493-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="1f493-117">Para obter mais informações relacionadas à opção de **\_ configuração/app** , consulte arquivo de [configuração de aplicativo (ACF)](application-configuration-file-acf-.md) e [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="1f493-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f493-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f493-118">Examples</span></span>

<span data-ttu-id="1f493-119">**MIDL/app \_ config filename. idl**</span><span class="sxs-lookup"><span data-stu-id="1f493-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1f493-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f493-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f493-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="1f493-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




