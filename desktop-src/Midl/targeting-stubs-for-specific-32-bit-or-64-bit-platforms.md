---
title: Direcionando stubs para plataformas específicas de 32 bits ou 64 bits
description: Alguns dos recursos do Microsoft RPC e do MIDL 3,0 e dos compiladores posteriores são específicos da plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL plataformas de 32 bits
- MIDL plataformas de 64 bits
- MIDL de stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292534"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="dbbbb-106">Direcionando stubs para plataformas específicas de 32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="dbbbb-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="dbbbb-107">Alguns dos recursos do Microsoft RPC e do MIDL 3,0 e dos compiladores posteriores são específicos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="dbbbb-108">Como precaução, os compiladores MIDL 3,0 e posterior geram proteções que facilitam a verificação de compatibilidade durante a fase de compilação da C.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="dbbbb-109">O MIDL gera dois tipos de guardas: uma proteção dependente de plataforma (32 bits versus 64 bits) e uma proteção dependente de versão (dependência de conjunto de recursos).</span><span class="sxs-lookup"><span data-stu-id="dbbbb-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="dbbbb-110">Por exemplo, MIDL gera a seguinte proteção para evitar a compilação C de um stub de 32 bits para outras plataformas:</span><span class="sxs-lookup"><span data-stu-id="dbbbb-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="dbbbb-111">A proteção dependente de versão é disparada por um conjunto de recursos encontrados nos arquivos IDL processados e pela opção [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="dbbbb-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="dbbbb-112">Por exemplo, se a interface usar recursos com suporte apenas no WindowsÂ 2000 ou posterior, MIDL gerará uma proteção com o destino \_ é \_ NT50 \_ ou \_ macro posterior.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="dbbbb-113">As macros de proteção, definidas em Rpcndr. h, dependem da configuração de WINVER e \_ Win32 \_ winnt e são avaliadas pelo compilador C/C++.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="dbbbb-114">Se, em tempo de compilação C, você receber uma mensagem de erro indicando que precisa de uma plataforma específica para executar um stub, primeiro verifique se você não usou um recurso que não esteja disponível nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="dbbbb-115">Os recursos que disparam um determinado protetor são listados no corpo da proteção.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="dbbbb-116">No exemplo anterior, a opção de compilador-Oicf disparou a proteção.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="dbbbb-117">Os recursos notáveis desse tipo incluem a opção [**/robust**](-robust.md) e o \[ atributo [**async**](async.md) \] disponíveis no WindowsÂ 2000 e posterior, o construtor de tipo de [**pipe**](pipe.md) , a opção de compilador/OIF e os \[ atributos [**\_ marshaling do usuário**](user-marshal.md) \] e \[ [**Wire \_ Marshal**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="dbbbb-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="dbbbb-118">Os stubs que usam esses recursos não serão executados em sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="dbbbb-119">Se você souber que a plataforma de destino está correta para os recursos que está usando e ainda receber um erro, talvez seja necessário definir as variáveis de ambiente adequadamente.</span><span class="sxs-lookup"><span data-stu-id="dbbbb-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="dbbbb-120">**Para compilar para o WindowsÂ 2000 ou versões posteriores**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="dbbbb-121">Adicione esta linha ao seu makefile:</span><span class="sxs-lookup"><span data-stu-id="dbbbb-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="dbbbb-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbbbb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbbbb-123">**/debug**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-124">**/robust**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-125">**Async**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-126">**\_UUID assíncrono**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-128">**pipe**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-129">**\_marshaling de transmissão**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-130">**Marshal do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="dbbbb-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="dbbbb-131">Empacotamento de tipos de dados OLE</span><span class="sxs-lookup"><span data-stu-id="dbbbb-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




