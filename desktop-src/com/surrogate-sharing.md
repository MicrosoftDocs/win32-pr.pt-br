---
title: Compartilhamento substituto
description: Os servidores DLL compartilharão um substituto se tiverem identidades de segurança correspondentes e compartilharem o mesmo valor AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635543"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="b9845-103">Compartilhamento substituto</span><span class="sxs-lookup"><span data-stu-id="b9845-103">Surrogate Sharing</span></span>

<span data-ttu-id="b9845-104">Os servidores DLL compartilharão um substituto se tiverem identidades de segurança correspondentes e compartilharem o mesmo valor AppID.</span><span class="sxs-lookup"><span data-stu-id="b9845-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="b9845-105">Os servidores DLL são carregados, por padrão, em seu próprio processo substituto.</span><span class="sxs-lookup"><span data-stu-id="b9845-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="b9845-106">Para carregar outros servidores DLL em um substituto existente para que ele dê suporte a mais de um servidor DLL, há dois requisitos:</span><span class="sxs-lookup"><span data-stu-id="b9845-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="b9845-107">Os servidores DLL devem ter o mesmo valor AppID.</span><span class="sxs-lookup"><span data-stu-id="b9845-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="b9845-108">O contexto de segurança dos servidores DLL deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="b9845-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="b9845-109">Se dois servidores DLL forem iniciados em diferentes identidades de segurança, eles deverão estar em diferentes substitutos, se seus AppIDs corresponderem.</span><span class="sxs-lookup"><span data-stu-id="b9845-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="b9845-110">Veja a seguir um exemplo de administração de compartilhamento substituto com AppIDs:</span><span class="sxs-lookup"><span data-stu-id="b9845-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="b9845-111">Os dois CLSIDs para componentes DLL comp1.dll e comp2.dll foram configurados para compartilhar uma AppID.</span><span class="sxs-lookup"><span data-stu-id="b9845-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="b9845-112">A chave [AppID](appid-key.md) especifica que o servidor DLL pode ser carregado em um substituto, especificando o valor [DllSurrogate](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="b9845-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="b9845-113">Neste exemplo, o valor de **DllSurrogate** é uma cadeia de caracteres vazia, indicando que a implementação de sistema padrão do substituto de DLL deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="b9845-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9845-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9845-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9845-115">Requisitos do servidor DLL</span><span class="sxs-lookup"><span data-stu-id="b9845-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="b9845-116">Registrando o servidor DLL para ativação alternativa</span><span class="sxs-lookup"><span data-stu-id="b9845-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




