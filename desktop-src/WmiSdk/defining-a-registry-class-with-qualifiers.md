---
description: As classes usadas para manter os dados do registro são definidas com vários qualificadores padrão.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definindo uma classe de registro com qualificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827843"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="cd81e-103">Definindo uma classe de registro com qualificadores</span><span class="sxs-lookup"><span data-stu-id="cd81e-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="cd81e-104">As classes usadas para manter os dados do registro são definidas com vários qualificadores padrão.</span><span class="sxs-lookup"><span data-stu-id="cd81e-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="cd81e-105">Veja a seguir uma lista dos qualificadores padrão:</span><span class="sxs-lookup"><span data-stu-id="cd81e-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="cd81e-106">[Dinâmico](standard-wmi-qualifiers.md) e [ **provedor**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="cd81e-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="cd81e-107">Você pode anexar o qualificador **dinâmico** a uma classe ou uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd81e-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="cd81e-108">O qualificador **dinâmico** marca a classe ou instância como gerenciada dinamicamente por um provedor.</span><span class="sxs-lookup"><span data-stu-id="cd81e-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="cd81e-109">Quando **dinâmico** aparece em uma classe ou instância, o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) também deve aparecer.</span><span class="sxs-lookup"><span data-stu-id="cd81e-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="cd81e-110">O qualificador do **provedor** identifica o provedor específico que deve gerenciar a classe ou instância dinâmica.</span><span class="sxs-lookup"><span data-stu-id="cd81e-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="cd81e-111">ClassContext</span><span class="sxs-lookup"><span data-stu-id="cd81e-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="cd81e-112">O qualificador **ClassContext** é anexado a uma classe.</span><span class="sxs-lookup"><span data-stu-id="cd81e-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="cd81e-113">Especifica o caminho para a chave do registro que contém as informações que a classe representa.</span><span class="sxs-lookup"><span data-stu-id="cd81e-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="cd81e-114">O qualificador **ClassContext** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="cd81e-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="cd81e-115">O valor de KeyPath poderá ser longo se incluir chaves com subchaves.</span><span class="sxs-lookup"><span data-stu-id="cd81e-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="cd81e-116">O exemplo a seguir mostra o qualificador **ClassContext** que contém o caminho para um dispositivo de transporte de computador específico.</span><span class="sxs-lookup"><span data-stu-id="cd81e-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="cd81e-117">O modelo a seguir para uma definição de classe ilustra o uso dos qualificadores **dinâmico**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="cd81e-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="cd81e-118">O provedor chamado pelo qualificador do **provedor** é o provedor de registro do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="cd81e-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="cd81e-119">Lembre-se de que os caminhos do registro não diferenciam maiúsculas de minúsculas, assim como os nomes do qualificador.</span><span class="sxs-lookup"><span data-stu-id="cd81e-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="cd81e-120">Os aplicativos de gerenciamento também podem usar o provedor de registro do sistema para recuperar e modificar dados de registro para uma chave específica.</span><span class="sxs-lookup"><span data-stu-id="cd81e-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



