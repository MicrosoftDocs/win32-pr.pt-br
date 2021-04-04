---
title: Criando e mantendo um ponto de conexão de serviço
description: Ao publicar com um SCP, lembre-se de que ele deve conter dados atuais sobre a instância do serviço.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Criando e mantendo um anúncio de ponto de conexão de serviço
- ponto de conexão de serviço AD, criando e mantendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007337"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="24bc0-105">Criando e mantendo um ponto de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="24bc0-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="24bc0-106">Ao publicar com um SCP, lembre-se de que ele deve conter dados atuais sobre a instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="24bc0-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="24bc0-107">Caso contrário, os clientes que se associam ao SCP recuperam dados desatualizados.</span><span class="sxs-lookup"><span data-stu-id="24bc0-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="24bc0-108">Seu instalador de serviço, que cria um SCP, especifica os valores iniciais para os atributos SCPs.</span><span class="sxs-lookup"><span data-stu-id="24bc0-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="24bc0-109">Em seguida, quando a instância do serviço é iniciada, ela deve localizar o SCP e atualizar os valores de atributo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="24bc0-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="24bc0-110">Dessa forma, os clientes estão garantidos os dados mais atuais.</span><span class="sxs-lookup"><span data-stu-id="24bc0-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="24bc0-111">Depois de criar o SCP, seu instalador de serviço executa duas etapas adicionais que permitem que seu serviço atualize o SCP:</span><span class="sxs-lookup"><span data-stu-id="24bc0-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="24bc0-112">Defina ACEs no descritor de segurança do objeto SCP para permitir que o serviço modifique os atributos do SCP em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="24bc0-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="24bc0-113">Para obter mais informações e um exemplo de código, consulte [habilitando a conta de serviço para acessar as propriedades do SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="24bc0-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="24bc0-114">Armazene o **objectGUID** do SCP no registro no computador host do serviço.</span><span class="sxs-lookup"><span data-stu-id="24bc0-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="24bc0-115">O serviço recupera o GUID armazenado em cache para associar ao SCP para verificar e atualizar seus atributos.</span><span class="sxs-lookup"><span data-stu-id="24bc0-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="24bc0-116">O instalador do serviço armazena em cache o **objectGUID** do SCP em vez de seu DN.</span><span class="sxs-lookup"><span data-stu-id="24bc0-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="24bc0-117">O **objectGUID** nunca muda, independentemente de o SCP ser movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="24bc0-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="24bc0-118">O DN pode ser alterado se um administrador mover ou renomear o SCP.</span><span class="sxs-lookup"><span data-stu-id="24bc0-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="24bc0-119">Por exemplo, se você criar um SCP como um filho de um objeto de computador, o nome distinto do SCP será alterado se o computador for renomeado ou movido para um domínio ou unidade organizacional diferente.</span><span class="sxs-lookup"><span data-stu-id="24bc0-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="24bc0-120">Quando um instalador do serviço cria um SCP, ele deve ler o **objectGUID** do objeto recém-criado e armazená-lo no registro do computador host do serviço.</span><span class="sxs-lookup"><span data-stu-id="24bc0-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="24bc0-121">Use o método [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) para obter o valor **objectGUID** no formato de cadeia de caracteres adequado para associação.</span><span class="sxs-lookup"><span data-stu-id="24bc0-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="24bc0-122">Armazene a cadeia de caracteres GUID como um valor na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="24bc0-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="24bc0-123">Em que "nome do fornecedor" e "nome do produto" identificam o fornecedor e o produto.</span><span class="sxs-lookup"><span data-stu-id="24bc0-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="24bc0-124">Quando o serviço é iniciado, ele recupera a cadeia de caracteres GUID armazenada em cache do registro e a usa para associar ao SCP.</span><span class="sxs-lookup"><span data-stu-id="24bc0-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="24bc0-125">O serviço lê os atributos de SCP importantes e os compara com os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="24bc0-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="24bc0-126">Se os valores de SCP estiverem desatualizados, o serviço os atualizará.</span><span class="sxs-lookup"><span data-stu-id="24bc0-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="24bc0-127">Os valores que o serviço pode exigir para atualizar incluem **palavras-chave**, **ServiceBindingInformation**, **serviceDNSName** e **serviceDNSNameType**.</span><span class="sxs-lookup"><span data-stu-id="24bc0-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="24bc0-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24bc0-128">Examples</span></span>

-   [<span data-ttu-id="24bc0-129">Exemplos de script</span><span class="sxs-lookup"><span data-stu-id="24bc0-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="24bc0-130">Exemplos de código (C/C++)</span><span class="sxs-lookup"><span data-stu-id="24bc0-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 