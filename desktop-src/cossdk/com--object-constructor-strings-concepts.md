---
description: As cadeias de caracteres do construtor do objeto COM+ são cadeias de inicialização que são especificadas administrativamente para um componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceitos de cadeias de caracteres do construtor de objeto COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920257"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="bb042-103">Conceitos de cadeias de caracteres do construtor de objeto COM+</span><span class="sxs-lookup"><span data-stu-id="bb042-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="bb042-104">As cadeias de caracteres do construtor do objeto COM+ são cadeias de inicialização que são especificadas administrativamente para um componente.</span><span class="sxs-lookup"><span data-stu-id="bb042-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="bb042-105">Você pode usar cadeias de caracteres de construtor de objeto para escrever um único componente com um grau de generalidade que permita que ele seja personalizado posteriormente para uma tarefa específica; ou seja, você pode executar a construção de objeto com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bb042-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="bb042-106">Por exemplo, você pode usar esse recurso para gravar um componente que contém uma conexão ODBC genérica e, posteriormente, especificar um DSN exato para o componente de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="bb042-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="bb042-107">Se a configuração do sistema for alterada, você poderá alterar a cadeia de caracteres do construtor de acordo.</span><span class="sxs-lookup"><span data-stu-id="bb042-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="bb042-108">As cadeias de caracteres do construtor de objeto não devem ser usadas para armazenar informações confidenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="bb042-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="bb042-109">Você pode usar cadeias de caracteres de construtor de objetos em conjunto com o [pool de objetos](com--object-pooling.md) para atingir um grau maior de granularidade em como pool e reutilizar recursos.</span><span class="sxs-lookup"><span data-stu-id="bb042-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="bb042-110">Por exemplo, você pode criar vários componentes distintos, idênticos, exceto para cadeias de caracteres de construtor e CLSIDs, para manter pools distintos de objetos que contêm conexões utilizáveis por grupos distintos de clientes.</span><span class="sxs-lookup"><span data-stu-id="bb042-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="bb042-111">Isso seria útil se as conexões fossem abertas de uma maneira que as associe a funções de segurança específicas — por exemplo, quando as conexões são abertas com alguma autenticação específica no banco de dados, Renderizando-as não reutilizáveis no caso geral.</span><span class="sxs-lookup"><span data-stu-id="bb042-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="bb042-112">Para fazer isso, você pode escrever um único componente genérico que se baseia em cadeias de caracteres do construtor de objetos, usando [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)e recompilá-lo para produzir vários componentes personalizáveis, cada um com um CLSID distinto.</span><span class="sxs-lookup"><span data-stu-id="bb042-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="bb042-113">Em seguida, você pode personalizar administrativamente cada componente para abrir uma conexão apropriada com uma cadeia de caracteres de construtor, configurá-los para serem agrupados e eles serão mantidos em pools distintos por CLSID.</span><span class="sxs-lookup"><span data-stu-id="bb042-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="bb042-114">Você pode especificar uma cadeia de caracteres de Construtor quando um componente tiver sido gravado especificamente para reconhecer a cadeia de caracteres inserida.</span><span class="sxs-lookup"><span data-stu-id="bb042-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="bb042-115">Os componentes podem acessar essas cadeias de caracteres programaticamente usando [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span><span class="sxs-lookup"><span data-stu-id="bb042-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="bb042-116">As cadeias de caracteres do Construtor são passadas no momento da criação do objeto quando a construção do objeto está habilitada administrativamente.</span><span class="sxs-lookup"><span data-stu-id="bb042-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="bb042-117">O COM+ chama o método [**constructodeobjetoi:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que ele implementa.</span><span class="sxs-lookup"><span data-stu-id="bb042-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="bb042-118">Dentro desse método, você pode acessar a cadeia de caracteres do construtor usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span><span class="sxs-lookup"><span data-stu-id="bb042-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="bb042-119">Cadeias de caracteres vazias podem ser entradas válidas.</span><span class="sxs-lookup"><span data-stu-id="bb042-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb042-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb042-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb042-121">Pool de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="bb042-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="bb042-122">Especificando uma cadeia de caracteres de construtor de objeto para um componente</span><span class="sxs-lookup"><span data-stu-id="bb042-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="bb042-123">Usando uma cadeia de caracteres de construtor de objeto para construir um componente</span><span class="sxs-lookup"><span data-stu-id="bb042-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



