---
title: Formatos de nome para SPNs exclusivos
description: Um SPN deve ser exclusivo na floresta em que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nome para anúncio de SPNs exclusivos
- ANÚNCIO do nome da entidade de serviço, formatos de nome para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159310"
---
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="ec5ac-105">Formatos de nome para SPNs exclusivos</span><span class="sxs-lookup"><span data-stu-id="ec5ac-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="ec5ac-106">Um SPN deve ser exclusivo na floresta em que está registrado.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="ec5ac-107">Se não for exclusivo, haverá falha na autenticação.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="ec5ac-108">A sintaxe de SPN tem quatro elementos: dois elementos necessários e dois elementos adicionais que você pode usar, se necessário, para produzir um nome exclusivo, conforme listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec5ac-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="ec5ac-109">Element</span></span></th>
<th><span data-ttu-id="ec5ac-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec5ac-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec5ac-111">&quot;&lt;classe de serviço&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="ec5ac-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="ec5ac-112">Uma cadeia de caracteres que identifica a classe geral do serviço; por exemplo, &quot; SqlServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="ec5ac-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="ec5ac-113">Há nomes de classe de serviço bem conhecidos, como &quot; www &quot; para um serviço Web ou &quot; LDAP &quot; para um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="ec5ac-114">Em geral, isso pode ser qualquer cadeia de caracteres que seja exclusiva para a classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="ec5ac-115">Lembre-se de que a sintaxe SPN usa uma barra (/) para separar elementos, portanto, esse caractere não pode aparecer em um nome de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec5ac-116">&quot;&lt;hospedeira&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="ec5ac-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="ec5ac-117">O nome do computador no qual o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="ec5ac-118">Pode ser um nome DNS totalmente qualificado ou um nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="ec5ac-119">Saiba que não há garantia de que os nomes NetBIOS serão exclusivos em uma floresta; portanto, um SPN que contém um nome NetBIOS pode não ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec5ac-120">&quot;&lt;porta&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="ec5ac-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="ec5ac-121">Um número de porta opcional para diferenciar entre várias instâncias da mesma classe de serviço em um único computador host.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="ec5ac-122">Omita esse componente se o serviço usar a porta padrão para sua classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec5ac-123">&quot;&lt;nome do serviço&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="ec5ac-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="ec5ac-124">Um nome opcional usado nos SPNs de um serviço replicável para identificar os dados ou serviços fornecidos pelo serviço ou pelo domínio servido pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="ec5ac-125">Este componente pode ter um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="ec5ac-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="ec5ac-126">O nome distinto ou objectGUID de um objeto em Active Directory Domain Services, como um SCP (ponto de conexão de serviço).</span><span class="sxs-lookup"><span data-stu-id="ec5ac-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="ec5ac-127">O nome DNS do domínio para um serviço que fornece um serviço especificado para um domínio como um todo.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="ec5ac-128">O nome DNS de um registro SRV ou MX.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ec5ac-129">Os componentes presentes nos SPNs de um serviço dependem de como o serviço é identificado e replicado.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="ec5ac-130">Há dois cenários básicos: serviços baseados em host e serviços replicáveis.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="ec5ac-131">Serviços baseados em host</span><span class="sxs-lookup"><span data-stu-id="ec5ac-131">Host-based services</span></span>

<span data-ttu-id="ec5ac-132">Para um serviço baseado em host, o &lt; componente "nome &gt; do serviço" é omitido porque o serviço é identificado exclusivamente pela classe de serviço e o nome do computador host no qual o serviço está instalado.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="ec5ac-133">A classe de serviço sozinha é suficiente para identificar para clientes os recursos que o serviço fornece.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="ec5ac-134">Você pode instalar instâncias da classe de serviço em vários computadores e cada instância fornece serviços que são identificados com seu computador host.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="ec5ac-135">FTP e Telnet são exemplos de serviços baseados em host.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="ec5ac-136">Os SPNs de uma instância de serviço baseada em host podem incluir o número da porta se o serviço usar uma porta não padrão ou se houver várias instâncias do serviço no host.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="ec5ac-137">Serviços replicáveis</span><span class="sxs-lookup"><span data-stu-id="ec5ac-137">Replicable services</span></span>

<span data-ttu-id="ec5ac-138">Para um serviço replicável pode haver uma ou mais instâncias do serviço (réplicas), e os clientes não diferenciam a qual réplica eles se conectam porque cada uma fornece o mesmo serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="ec5ac-139">Os SPNs de cada réplica têm os mesmos componentes de " &lt; classe &gt; de serviço" e " &lt; nome do serviço &gt; ", em que " &lt; nome &gt; do serviço" identifica mais especificamente os recursos fornecidos pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="ec5ac-140">Somente os &lt; componentes "host &gt; " e " &lt; porta" opcional &gt; variam de SPN para SPN.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="ec5ac-141">Um exemplo de um serviço replicável seria uma instância de um serviço de banco de dados que fornece acesso a um banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="ec5ac-142">Nesse caso, " &lt; classe de serviço &gt; " identifica o aplicativo de banco de dados e " &lt; nome &gt; do serviço" identifica o banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="ec5ac-143">" &lt; nome &gt; do serviço" pode ser o nome distinto de um SCP (ponto de conexão de serviço) que contém dados de conexão para o banco de dado.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="ec5ac-144">Se os clientes usarem o nome NetBIOS para compor o SPN de um serviço, cada réplica também deverá registrar um SPN que contenha o nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="ec5ac-145">Outro exemplo de um serviço replicável é aquele que fornece serviços a um domínio inteiro.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="ec5ac-146">Nesse caso, o componente " &lt; nome do serviço &gt; " é o nome DNS do domínio que está sendo servido.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="ec5ac-147">Um KDC Kerberos é um exemplo desse tipo de serviço replicável.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="ec5ac-148">Lembre-se de que, se o nome DNS de um computador for alterado, o sistema atualizará o &lt; elemento "host &gt; " para todos os SPNs registrados para esse host na floresta.</span><span class="sxs-lookup"><span data-stu-id="ec5ac-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




