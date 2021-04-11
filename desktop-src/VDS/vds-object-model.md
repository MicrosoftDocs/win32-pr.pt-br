---
description: Modelo de objeto VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modelo de objeto VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172390"
---
# <a name="vds-object-model"></a><span data-ttu-id="a4528-103">Modelo de objeto VDS</span><span class="sxs-lookup"><span data-stu-id="a4528-103">VDS Object Model</span></span>

<span data-ttu-id="a4528-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a4528-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="a4528-105">O VDS fornece acesso indireto a dispositivos de armazenamento baseados em host, como discos e dispositivos de CD-ROM, e a matrizes de disco que são gerenciadas por controladores RAID de hardware.</span><span class="sxs-lookup"><span data-stu-id="a4528-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="a4528-106">Enquanto algumas entidades de armazenamento modelam dispositivos físicos, outros modelam construções virtuais: volumes, partições e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a4528-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="a4528-107">Os objetos descritos neste tópico representam as entidades físicas e virtuais do VDS.</span><span class="sxs-lookup"><span data-stu-id="a4528-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="a4528-108">Os aplicativos chamam os métodos que são expostos por esses objetos e o VDS chama o provedor apropriado para executar as operações de armazenamento solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a4528-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="a4528-109">Um aplicativo nunca chama um programa de provedor diretamente.</span><span class="sxs-lookup"><span data-stu-id="a4528-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="a4528-110">Classificação de objetos</span><span class="sxs-lookup"><span data-stu-id="a4528-110">Classification of Objects</span></span>

<span data-ttu-id="a4528-111">Como mostra a ilustração a seguir, os programas de provedor de software implementam objetos que modelam entidades baseadas em host; programas de provedor de hardware implementam objetos que modelam dispositivos RAID de hardware internos e externos; os objetos comuns restantes são independentes do provedor ou são implementados pelo VDS.</span><span class="sxs-lookup"><span data-stu-id="a4528-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="a4528-112">Um eixo, que não é um objeto VDS, é um termo para mídia de armazenamento genérico que compreende as extensões de disco ou unidade.</span><span class="sxs-lookup"><span data-stu-id="a4528-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Diagrama que mostra uma classificação de objetos, definidos como ' objetos comuns ', ' objetos de provedor de software ' e ' objetos de provedor de hardware '.](images/vdsobjectmodel.png)

<span data-ttu-id="a4528-114">Para saber mais sobre o comportamento de cada objeto, selecione um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a4528-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="a4528-115">Carregador de serviço e objetos de serviço, consulte [Startup and Service Objects](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4528-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="a4528-116">Enumeração e objetos assíncronos, consulte [objetos auxiliares](helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4528-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="a4528-117">Objeto do provedor, consulte [objeto do provedor](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="a4528-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="a4528-118">Objetos de pacote, disco, volume e volume Plex, consulte [objetos de provedor de software](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4528-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="a4528-119">Objetos de subsistema, controlador, unidade, LUN e LUN Plex, consulte [objetos de provedor de hardware](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4528-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="a4528-120">Criação de objetos</span><span class="sxs-lookup"><span data-stu-id="a4528-120">Object Creation</span></span>

<span data-ttu-id="a4528-121">As operações de configuração e consulta associadas à criação de objetos podem levar um tempo considerável para serem concluídas; dessa forma, o VDS invoca todos os métodos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a4528-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="a4528-122">O provedor de descoberta retorna todos os eventos de conclusão, erro ou alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="a4528-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="a4528-123">Os provedores de software também registram em log todos os erros e alterações de estado significativas.</span><span class="sxs-lookup"><span data-stu-id="a4528-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="a4528-124">Exclusão de objeto</span><span class="sxs-lookup"><span data-stu-id="a4528-124">Object Deletion</span></span>

<span data-ttu-id="a4528-125">Vários métodos VDS excluem ou transformam objetos VDS.</span><span class="sxs-lookup"><span data-stu-id="a4528-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="a4528-126">Um chamador pode manter uma referência, por meio de um ponteiro de interface, para um objeto excluído depois que o método retorna.</span><span class="sxs-lookup"><span data-stu-id="a4528-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="a4528-127">Quando o chamador libera a interface, o VDS exclui o objeto.</span><span class="sxs-lookup"><span data-stu-id="a4528-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="a4528-128">Com relação à exclusão de objetos, os chamadores devem evitar invocar qualquer coisa, exceto o método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="a4528-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="a4528-129">O provedor deve ser robusto o suficiente para lidar com chamadores errônea; se um chamador invocar um método em um objeto excluído, o provedor deverá retornar **o \_ objeto VDS E \_ \_ excluído**.</span><span class="sxs-lookup"><span data-stu-id="a4528-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="a4528-130">Inicialização do serviço</span><span class="sxs-lookup"><span data-stu-id="a4528-130">Service Initialization</span></span>

<span data-ttu-id="a4528-131">O VDS fornece um identificador de classe (CLSID) para o carregador de serviço e os objetos de serviço, mas apenas o CLSID do carregador de serviço é público.</span><span class="sxs-lookup"><span data-stu-id="a4528-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="a4528-132">A inicialização do serviço ocorre quando os provedores, um aplicativo de chamada e o serviço executam as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a4528-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="a4528-133">Cada novo provedor invoca o método [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante a instalação para se registrar no VDS.</span><span class="sxs-lookup"><span data-stu-id="a4528-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="a4528-134">A chamada cria uma chave do registro no hive do sistema, identificada pelo GUID do objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="a4528-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="a4528-135">Contido nessa chave está o CLSID do objeto do provedor, o nome, a versão e o GUID da versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="a4528-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="a4528-136">Os GUIDs de objeto do provedor são persistentes; os GUIDs de objeto de software e hardware não são.</span><span class="sxs-lookup"><span data-stu-id="a4528-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="a4528-137">Um aplicativo chama a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , passando o CLSID do carregador de serviço como um argumento.</span><span class="sxs-lookup"><span data-stu-id="a4528-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="a4528-138">Com um ponteiro para o objeto do carregador de serviço, o aplicativo pode iniciar o VDS local ou remotamente passando o nome do computador desejado como um parâmetro para o método [**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .</span><span class="sxs-lookup"><span data-stu-id="a4528-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="a4528-139">Quando o aplicativo inicial é anexado ao serviço, o VDS primeiro chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em cada CLSID encontrado na chave do registro e, em seguida, chama o método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) em cada provedor para inicializar os programas.</span><span class="sxs-lookup"><span data-stu-id="a4528-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4528-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4528-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4528-141">Sobre o VDS</span><span class="sxs-lookup"><span data-stu-id="a4528-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="a4528-142">**IVdsAdmin:: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="a4528-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="a4528-143">**IVdsServiceLoader:: loadservice**</span><span class="sxs-lookup"><span data-stu-id="a4528-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="a4528-144">**IVdsProviderPrivate:: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="a4528-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
