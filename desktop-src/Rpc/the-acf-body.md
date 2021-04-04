---
title: O corpo de ACF
description: O corpo de ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104008513"
---
# <a name="the-acf-body"></a><span data-ttu-id="44284-103">O corpo de ACF</span><span class="sxs-lookup"><span data-stu-id="44284-103">The ACF Body</span></span>

<span data-ttu-id="44284-104">O corpo de ACF contém atributos de configuração que se aplicam a tipos e funções definidos no corpo da interface do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="44284-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="44284-105">O corpo do ACF pode estar vazio ou pode conter atributos de ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), Function e Parameter.</span><span class="sxs-lookup"><span data-stu-id="44284-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="44284-106">Todos esses itens são opcionais.</span><span class="sxs-lookup"><span data-stu-id="44284-106">All of these items are optional.</span></span> <span data-ttu-id="44284-107">Atributos aplicados a tipos individuais e funções no corpo de ACF substituem atributos no cabeçalho ACF.</span><span class="sxs-lookup"><span data-stu-id="44284-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="44284-108">O ACF especifica o comportamento no computador local e não afeta os dados transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="44284-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="44284-109">Ele é usado para especificar detalhes de um stub a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="44284-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="44284-110">No modo de compatibilidade DCE ([**/OSF**](/windows/desktop/Midl/-osf)), o ACF não afeta a interação entre os stubs, mas entre o stub e o código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44284-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="44284-111">Um parâmetro especificado no ACF deve ser um dos parâmetros especificados no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="44284-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="44284-112">A ordem de especificação do parâmetro no ACF não é significativa porque a correspondência é por nome, não pela posição.</span><span class="sxs-lookup"><span data-stu-id="44284-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="44284-113">A lista de parâmetros no ACF pode estar vazia, mesmo quando a lista de parâmetros na assinatura IDL correspondente não é (mas não é recomendável).</span><span class="sxs-lookup"><span data-stu-id="44284-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="44284-114">Os declaradores abstratos (parâmetros sem nome) no arquivo IDL fazem com que o compilador MIDL Relate erros durante o processamento do ACF porque o parâmetro não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="44284-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="44284-115">A diretiva ACF **include** especifica os arquivos de cabeçalho a serem exibidos no cabeçalho gerado como parte de uma instrução de **\# inclusão** padrão do C-pré-processador.</span><span class="sxs-lookup"><span data-stu-id="44284-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="44284-116">A palavra-chave ACF **inclui** difere de uma diretiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="44284-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="44284-117">A palavra-chave ACF **include** faz com que a linha "**\# include** *filename*" apareça no arquivo de cabeçalho gerado, enquanto a diretiva C-Language "**\# include** *filename*" faz com que o conteúdo desse arquivo seja colocado no ACF.</span><span class="sxs-lookup"><span data-stu-id="44284-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="44284-118">A instrução de [**typedef**](/windows/desktop/Midl/typedef) de ACF permite aplicar atributos de tipo de ACF a tipos definidos anteriormente no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="44284-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="44284-119">A sintaxe de **typedef** de ACF difere da sintaxe de **typedef** C.</span><span class="sxs-lookup"><span data-stu-id="44284-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="44284-120">Os atributos da função ACF permitem que você especifique atributos que se aplicam à função como um todo.</span><span class="sxs-lookup"><span data-stu-id="44284-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="44284-121">Para obter mais informações, consulte **\[** [**código**](/windows/desktop/Midl/code) **\]** , **\[** [**otimizar**](/windows/desktop/Midl/optimize) **\]** e **\[** [**Nocode**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="44284-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="44284-122">Os atributos de parâmetro de ACF permitem especificar atributos que se aplicam a parâmetros individuais da função.</span><span class="sxs-lookup"><span data-stu-id="44284-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="44284-123">Para obter mais informações, consulte **\[** [**\_ contagem de bytes**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="44284-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44284-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44284-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44284-125">**configuração do/App \_**</span><span class="sxs-lookup"><span data-stu-id="44284-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="44284-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="44284-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="44284-127">[**\[\_identificador automático\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="44284-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="44284-128">[**\[auto-completar\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="44284-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="44284-129">[**\[\_identificador explícito\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="44284-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="44284-130">O arquivo IDL (Interface Definition Language)</span><span class="sxs-lookup"><span data-stu-id="44284-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="44284-131">[**\[\_identificador implícito\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="44284-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="44284-132">**incluir**</span><span class="sxs-lookup"><span data-stu-id="44284-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="44284-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="44284-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="44284-134">[**\[Nocode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="44284-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="44284-135">[**\[formato\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="44284-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="44284-136">[**\[representar \_ como\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="44284-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="44284-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="44284-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 