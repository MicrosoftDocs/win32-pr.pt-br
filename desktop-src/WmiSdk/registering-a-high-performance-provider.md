---
description: Assim como outros provedores de instância, você registra um provedor de alto desempenho com o Microsoft Windows&\# 160; Instrumentação de gerenciamento (WMI) criando uma instância das \_ \_ classes Win32Provider e \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrando um provedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010763"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="99328-103">Registrando um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="99328-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="99328-104">Assim como outros provedores de instância, você registra um provedor de alto desempenho com o Microsoft Instrumentação de gerenciamento do Windows (WMI) criando uma instância das classes [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="99328-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="99328-105">A instância do **\_ \_ Win32Provider** define a implementação física do provedor e a instância **\_ \_ InstanceProviderRegistration** define o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="99328-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="99328-106">Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="99328-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="99328-107">O procedimento a seguir descreve como registrar um provedor de instância de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="99328-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="99328-108">**Para registrar um provedor de instância de alto desempenho**</span><span class="sxs-lookup"><span data-stu-id="99328-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="99328-109">Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.</span><span class="sxs-lookup"><span data-stu-id="99328-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="99328-110">Certifique-se de adicionar uma propriedade **ClientLoadableCLSID** à instância [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="99328-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="99328-111">Se o provedor e o cliente residirem no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="99328-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="99328-112">Quando o provedor e o cliente residem em computadores diferentes, o WMI carrega o provedor em processo para o WMI.</span><span class="sxs-lookup"><span data-stu-id="99328-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="99328-113">O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.</span><span class="sxs-lookup"><span data-stu-id="99328-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="99328-114">Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que descreve o conjunto de recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="99328-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="99328-115">Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="99328-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="99328-116">O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="99328-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="99328-117">O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.</span><span class="sxs-lookup"><span data-stu-id="99328-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="99328-118">Um provedor de alto desempenho também precisa de um estado de suporte para operações, operações de enumeração ou ambos.</span><span class="sxs-lookup"><span data-stu-id="99328-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="99328-119">Certifique-se de usar as propriedades **SupportsGet** e **SupportsEnumeration** em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="99328-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="99328-120">O exemplo de código a seguir mostra como implementar as classes [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) para um provedor de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="99328-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="99328-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99328-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99328-122">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="99328-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



