---
title: Publicando com pontos de conexão de serviço
description: O esquema de Active Directory define uma classe de objeto serviceConnectionPoint (SCP) para tornar mais fácil para um serviço publicar dados específicos do serviço no diretório.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publicando com pontos de conexão de serviço AD
- AD de pontos de conexão de serviço
- pontos de conexão de serviço AD, publicando com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634927"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="f7c98-106">Publicando com pontos de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="f7c98-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="f7c98-107">O esquema de Active Directory define uma classe de objeto **serviceConnectionPoint** (SCP) para tornar mais fácil para um serviço publicar dados específicos do serviço no diretório.</span><span class="sxs-lookup"><span data-stu-id="f7c98-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="f7c98-108">Os clientes do serviço usam os dados em um SCP para localizar, conectar e autenticar uma instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7c98-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="f7c98-109">Esta seção fornece uma visão geral dos pontos de conexão de serviço e exemplos de código que mostram como um aplicativo cliente/serviço usa o SCPs.</span><span class="sxs-lookup"><span data-stu-id="f7c98-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="f7c98-110">O exemplo de código segue estas etapas para implementar a publicação de serviço com SCPs.</span><span class="sxs-lookup"><span data-stu-id="f7c98-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="f7c98-111">Para obter mais informações e um exemplo de código que executa essas etapas, consulte [criando um ponto de conexão de serviço](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="f7c98-112">**Para criar SCPs no diretório na instalação do serviço**</span><span class="sxs-lookup"><span data-stu-id="f7c98-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="f7c98-113">Associe-se ao objeto de computador do computador host no qual a instância de serviço está instalada.</span><span class="sxs-lookup"><span data-stu-id="f7c98-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="f7c98-114">Crie um objeto SCP como um filho do objeto Computer, especificando os valores iniciais para os atributos do SCP.</span><span class="sxs-lookup"><span data-stu-id="f7c98-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="f7c98-115">Defina as ACEs (entradas de controle de acesso) no descritor de segurança do objeto SCP para permitir que o serviço modifique as propriedades do SCP em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f7c98-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="f7c98-116">Armazene o **objectGUID** do SCP no registro no computador host do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7c98-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="f7c98-117">Para obter mais informações e um exemplo de código que executa essas etapas, consulte [atualizando um ponto de conexão de serviço](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="f7c98-118">**Para atualizar os atributos do SCP na inicialização do serviço**</span><span class="sxs-lookup"><span data-stu-id="f7c98-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="f7c98-119">Recupere o **objectGUID** do registro e use-o para associar ao scp.</span><span class="sxs-lookup"><span data-stu-id="f7c98-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="f7c98-120">Recupere atributos, como **serviceDNSName** e **SERVICEBINDINGINFORMATION**, do SCP.</span><span class="sxs-lookup"><span data-stu-id="f7c98-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="f7c98-121">Compare esses valores com os valores atuais e atualize o SCP, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f7c98-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="f7c98-122">Para obter mais informações e um exemplo de código que executa essas etapas, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="f7c98-123">**Para localizar e usar um SCP por um aplicativo cliente**</span><span class="sxs-lookup"><span data-stu-id="f7c98-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="f7c98-124">Associe-se ao catálogo global e pesquise objetos com um atributo de **palavras-chave** que corresponda ao GUID do produto do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7c98-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="f7c98-125">Cada objeto encontrado é uma instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7c98-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="f7c98-126">Selecione uma instância e recupere o nome distinto do SCP.</span><span class="sxs-lookup"><span data-stu-id="f7c98-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="f7c98-127">Use o nome distinto para associar ao SCP.</span><span class="sxs-lookup"><span data-stu-id="f7c98-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="f7c98-128">Recupere os valores de vários atributos do SCP, como **serviceDNSName** e **ServiceBindingInformation**.</span><span class="sxs-lookup"><span data-stu-id="f7c98-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="f7c98-129">Use esses valores para se conectar e autenticar a instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7c98-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="f7c98-130">Para obter mais informações sobre quais funções podem criar e atualizar um SCP, consulte [problemas de segurança para publicação de serviço](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="f7c98-131">Para obter mais informações sobre onde criar um SCP, consulte [onde criar um ponto de conexão de serviço](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="f7c98-132">Para obter mais informações sobre o tipo de dados a ser armazenado em um SCP, consulte [Propriedades do ponto de conexão de serviço](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="f7c98-133">Para obter mais informações sobre como um instalador de serviço e o serviço funcionam em conjunto para manter os dados atuais em um SCP, consulte [criando e mantendo um ponto de conexão de serviço](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7c98-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




