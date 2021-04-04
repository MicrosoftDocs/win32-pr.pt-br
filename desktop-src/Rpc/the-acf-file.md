---
title: O arquivo ACF
description: O arquivo ACF permite que você personalize a interface RPC de seus aplicativos cliente e/ou servidor sem afetar as características de rede da interface.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917633"
---
# <a name="the-acf-file"></a><span data-ttu-id="6b030-103">O arquivo ACF</span><span class="sxs-lookup"><span data-stu-id="6b030-103">The ACF File</span></span>

<span data-ttu-id="6b030-104">O arquivo ACF permite que você personalize a interface RPC de seus aplicativos cliente e/ou servidor sem afetar as características de rede da interface.</span><span class="sxs-lookup"><span data-stu-id="6b030-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="6b030-105">Por exemplo, se o aplicativo cliente contiver uma estrutura de dados complexa que tenha apenas significado no computador local, você poderá especificar no arquivo ACF como os dados nessa estrutura podem ser representados em um formato independente de computador para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="6b030-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="6b030-106">Este tutorial demonstra outro uso do arquivo ACF, especificando o tipo de identificador de associação que representa a conexão entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="6b030-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="6b030-107">O **\[** [**atributo \_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** no cabeçalho ACF permite que o aplicativo cliente selecione um servidor para sua chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="6b030-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="6b030-108">O ACF define o identificador para ser do identificador de [**tipo \_ t**](/windows/desktop/Midl/handle-t) (um tipo de dados primitivo MIDL).</span><span class="sxs-lookup"><span data-stu-id="6b030-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="6b030-109">O compilador MIDL colocará o nome do identificador de associação que o ACF especificou, Hello \_ IfHandle no arquivo de cabeçalho gerado por ele.</span><span class="sxs-lookup"><span data-stu-id="6b030-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="6b030-110">Observe que esse arquivo ACF específico tem um corpo vazio.</span><span class="sxs-lookup"><span data-stu-id="6b030-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="6b030-111">O compilador MIDL tem uma opção, [**/app \_ config**](/windows/desktop/Midl/-app-config), que permite que você inclua determinados atributos de ACF, como o **\_ identificador implícito**, no arquivo IDL, em vez de criar um arquivo ACF separado.</span><span class="sxs-lookup"><span data-stu-id="6b030-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="6b030-112">Considere usar essa opção se seu aplicativo não exigir muita configuração especial e se a compatibilidade uso estrita não for um problema.</span><span class="sxs-lookup"><span data-stu-id="6b030-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 