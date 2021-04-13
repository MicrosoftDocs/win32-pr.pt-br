---
description: Os aplicativos COM+ consistem em um ou mais componentes COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Partes de um aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456952"
---
# <a name="parts-of-a-com-application"></a><span data-ttu-id="0a9b5-103">Partes de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="0a9b5-103">Parts of a COM+ Application</span></span>

<span data-ttu-id="0a9b5-104">Os aplicativos COM+ consistem em um ou mais componentes COM.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-104">COM+ applications consist of one or more COM components.</span></span>

<span data-ttu-id="0a9b5-105">Os seguintes termos são usados em toda a documentação do COM+:</span><span class="sxs-lookup"><span data-stu-id="0a9b5-105">The following terms are used throughout the COM+ documentation:</span></span>

<dl> <dt>

<span data-ttu-id="0a9b5-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*</span><span class="sxs-lookup"><span data-stu-id="0a9b5-106"><span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM component*</span></span>
</dt> <dd>

<span data-ttu-id="0a9b5-107">Uma unidade binária de código que cria objetos COM (inclui o código de empacotamento e de registro).</span><span class="sxs-lookup"><span data-stu-id="0a9b5-107">A binary unit of code that creates COM objects (includes packaging and registration code).</span></span>

</dd> <dt>

<span data-ttu-id="0a9b5-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objeto COM*</span><span class="sxs-lookup"><span data-stu-id="0a9b5-108"><span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM object*</span></span>
</dt> <dd>

<span data-ttu-id="0a9b5-109">Uma instância de uma classe COM.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-109">An instance of a COM class.</span></span>

</dd> <dt>

<span data-ttu-id="0a9b5-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*</span><span class="sxs-lookup"><span data-stu-id="0a9b5-110"><span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM class*</span></span>
</dt> <dd>

<span data-ttu-id="0a9b5-111">Uma implementação nomeada e concreta de uma ou mais interfaces.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-111">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="0a9b5-112">Uma classe COM é identificada por um CLSID (às vezes, por um ProgID também).</span><span class="sxs-lookup"><span data-stu-id="0a9b5-112">A COM class is identified by a CLSID (sometimes by a ProgID also).</span></span>

</dd> <dt>

<span data-ttu-id="0a9b5-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interface COM*</span><span class="sxs-lookup"><span data-stu-id="0a9b5-113"><span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM interface*</span></span>
</dt> <dd>

<span data-ttu-id="0a9b5-114">Um grupo de funções de método relacionadas exposto por uma classe COM que especifica um contrato.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-114">A group of related method functions exposed by a COM class that specify a contract.</span></span> <span data-ttu-id="0a9b5-115">Isso inclui o nome, a assinatura da interface, a semântica da interface e o formato do buffer de marshaling.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-115">This includes the name, interface signature, interface semantics, and marshaling buffer format.</span></span> <span data-ttu-id="0a9b5-116">Uma interface é identificada por um IID.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-116">An interface is identified by an IID.</span></span> <span data-ttu-id="0a9b5-117">A sintaxe da interface é definida nas bibliotecas IDL e/ou tipo.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-117">The interface syntax is defined in IDL and/or type libraries.</span></span> <span data-ttu-id="0a9b5-118">As interfaces de uma classe COM devem ser divididas em conjuntos de métodos coesas e gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-118">The interfaces of a COM class should be divided into manageable, cohesive sets of methods.</span></span>

<span data-ttu-id="0a9b5-119">Interfaces COM são imutáveis; o contrato COM indica que eles não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-119">COM interfaces are immutable; the COM contract states that they cannot be modified.</span></span> <span data-ttu-id="0a9b5-120">Qualquer modificação (como adicionar métodos) requer a definição de uma nova interface.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-120">Any modification (such as adding methods) requires defining a new interface.</span></span>

</dd> <dt>

<span data-ttu-id="0a9b5-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Método COM*</span><span class="sxs-lookup"><span data-stu-id="0a9b5-121"><span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM method*</span></span>
</dt> <dd>

<span data-ttu-id="0a9b5-122">Um de um conjunto de funções relacionadas fornecido por uma interface COM.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-122">One of a set of related functions provided by a COM interface.</span></span>

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a><span data-ttu-id="0a9b5-123">Componentes configurados e não configurados</span><span class="sxs-lookup"><span data-stu-id="0a9b5-123">Configured and Unconfigured Components</span></span>

<span data-ttu-id="0a9b5-124">Para tirar proveito dos serviços que os aplicativos COM+ dão suporte, o ambiente COM+ impõe requisitos específicos em componentes COM criados para aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-124">To take advantage of the services that COM+ applications support, the COM+ environment imposes specific requirements on COM components built for COM+ applications.</span></span> <span data-ttu-id="0a9b5-125">Quando adicionado a um aplicativo COM+, um componente COM é conhecido como um *componente configurado*.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-125">When added to a COM+ application, a COM component is known as a *configured component*.</span></span>

<span data-ttu-id="0a9b5-126">Os componentes COM criados para aplicativos COM+ são componentes de servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-126">COM components built for COM+ applications are in-process server components.</span></span> <span data-ttu-id="0a9b5-127">O componente deve conter uma biblioteca de tipos (arquivo. tlb) para descrever todas as classes implementadas no componente e declarar as interfaces em todas as classes no componente.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-127">The component must contain a type library (.tlb file) to describe all classes implemented in the component and declare the interfaces on all classes in the component.</span></span> <span data-ttu-id="0a9b5-128">Você pode criar e implementar esses componentes com o Microsoft Visual Basic, Microsoft Visual C++ ou qualquer ferramenta de desenvolvimento compatível COM COM.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-128">You can create and implement these components with Microsoft Visual Basic, Microsoft Visual C++, or any COM-compatible development tool.</span></span>

<span data-ttu-id="0a9b5-129">Um *componente não configurado* é um componente que não está instalado em um aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-129">An *unconfigured component* is a component that isn't installed in a COM+ application.</span></span> <span data-ttu-id="0a9b5-130">Você pode transformar a maioria dos componentes não configurados em componentes definidos simplesmente integrando-os em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-130">You can transform most unconfigured components into configured components simply by integrating them into a COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="0a9b5-131">Não use o mesmo AppID para um aplicativo COM+ e no registro para um componente não configurado.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-131">Do not use the same AppID for both a COM+ application and in the registry for an unconfigured component.</span></span> <span data-ttu-id="0a9b5-132">Quando o componente não configurado é ativado, uma vez que a ativação pode recuperar as informações do aplicativo COM+ do registro que não contém as informações necessárias para a ativação COM.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-132">When the unconfigured component is activated , as activation may retrieve the COM+ application information from the registry that does not contain the information required for COM activation.</span></span> <span data-ttu-id="0a9b5-133">Problemas semelhantes podem surgir se uma chamada for feita para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) do dllhost que hospeda o aplicativo do servidor do com+.</span><span class="sxs-lookup"><span data-stu-id="0a9b5-133">Similar problems could arise if a call is made to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) from DllHost that hosts COM+ Server application.</span></span>

 

 

 
