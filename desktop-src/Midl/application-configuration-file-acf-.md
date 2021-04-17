---
title: Arquivo de configuração de aplicativo (ACF)
description: Pode haver aspectos do seu aplicativo distribuído que afetam um componente, mas não têm nada a ver com outro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Linguagem IDL da Microsoft MIDL, descrito, arquivo de configuração de aplicativo
- arquivo de configuração de aplicativo MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748604"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="739ac-106">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="739ac-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="739ac-107">Pode haver aspectos do seu aplicativo distribuído que afetam um componente, mas não têm nada a ver com outro.</span><span class="sxs-lookup"><span data-stu-id="739ac-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="739ac-108">Por exemplo, um objeto pode conter uma estrutura de dados grande e complexa e passar o conteúdo dessa estrutura de dados para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="739ac-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="739ac-109">O layout exato dessa estrutura de dados pode não ser sentido para o aplicativo de recebimento.</span><span class="sxs-lookup"><span data-stu-id="739ac-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="739ac-110">Além disso, a estrutura pode conter tipos de dados que o compilador MIDL não reconhece e não pode gerar empacotamento e desempacotamento de código.</span><span class="sxs-lookup"><span data-stu-id="739ac-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="739ac-111">Os aplicativos cliente podem compartilhar a mesma interface, mas são executados em diferentes plataformas; Eles podem precisar de seu próprio conjunto de rotinas de marshaling.</span><span class="sxs-lookup"><span data-stu-id="739ac-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="739ac-112">Por fim, os clientes individuais talvez nem sempre precisem do mesmo conjunto de funções.</span><span class="sxs-lookup"><span data-stu-id="739ac-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="739ac-113">Não é eficiente gerar código stub para funções que nunca serão implementadas em um determinado aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="739ac-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="739ac-114">Ao definir esses aspectos locais de sua interface em um arquivo de configuração de aplicativo (ACF), você pode separar as diferenças entre as interfaces de cliente de sua representação de rede, permitindo que o servidor envie e receba dados em um formato consistente e tornando seu código stub mais compacto e eficiente.</span><span class="sxs-lookup"><span data-stu-id="739ac-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="739ac-115">A estrutura e a sintaxe de uma definição de interface ACF são idênticas à definição de IDL:</span><span class="sxs-lookup"><span data-stu-id="739ac-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="739ac-116">Por padrão, o nome da interface ACF deve corresponder ao seu nome na definição de IDL.</span><span class="sxs-lookup"><span data-stu-id="739ac-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="739ac-117">No entanto, quando você usa a opção de compilador MIDL/ [**ACF**](-acf.md) para especificar explicitamente um nome de arquivo ACF, os nomes de interface não precisam corresponder.</span><span class="sxs-lookup"><span data-stu-id="739ac-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="739ac-118">Esse recurso permite que várias interfaces compartilhem uma única especificação de ACF.</span><span class="sxs-lookup"><span data-stu-id="739ac-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




