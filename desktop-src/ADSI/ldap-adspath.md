---
title: ADsPath LDAP
description: Este tópico mostra a sintaxe que você deve usar para o ADsPath do LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- ADsPath LDAP
- ADsPath, LDAP, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641851"
---
# <a name="ldap-adspath"></a><span data-ttu-id="9b7ac-105">ADsPath LDAP</span><span class="sxs-lookup"><span data-stu-id="9b7ac-105">LDAP ADsPath</span></span>

<span data-ttu-id="9b7ac-106">O ADsPath do provedor LDAP da Microsoft requer o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-106">The Microsoft LDAP provider ADsPath requires the following format.</span></span>


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> <span data-ttu-id="9b7ac-107">Os caracteres de colchetes esquerdo e direito ( \[ \] ) indicam parâmetros opcionais; não é uma parte literal da cadeia de caracteres de associação.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-107">The left and right bracket characters (\[ \]) indicate optional parameters; it is not a literal part of the binding string.</span></span>

 

<span data-ttu-id="9b7ac-108">O "HostName" pode ser um nome de computador, um endereço IP ou um nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-108">The "HostName" can be a computer name, an IP address, or a domain name.</span></span> <span data-ttu-id="9b7ac-109">Um nome de servidor também pode ser especificado na cadeia de vinculação.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-109">A server name can also be specified in the binding string.</span></span> <span data-ttu-id="9b7ac-110">A maioria dos provedores LDAP segue um modelo que exige a especificação de um nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-110">Most LDAP providers follow a model that requires a server name to be specified.</span></span>

<span data-ttu-id="9b7ac-111">A "PortNumber" especifica a porta a ser usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-111">The "PortNumber" specifies the port to be used for the connection.</span></span> <span data-ttu-id="9b7ac-112">Se nenhum número de porta for especificado, o provedor LDAP usará o número da porta padrão.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-112">If no port number is specified, the LDAP provider uses the default port number.</span></span> <span data-ttu-id="9b7ac-113">O número da porta padrão será 389 se não estiver usando uma conexão SSL ou 636 se estiver usando uma conexão SSL.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-113">The default port number is 389 if not using an SSL connection or 636 if using an SSL connection.</span></span>

<span data-ttu-id="9b7ac-114">O "DistinguishedName" especifica o nome distinto de um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-114">The "DistinguishedName" specifies the distinguished name of a specific object.</span></span> <span data-ttu-id="9b7ac-115">É garantido que um nome distinto para um determinado objeto seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-115">A distinguished name for a given object is guaranteed to be unique.</span></span>

<span data-ttu-id="9b7ac-116">A tabela a seguir lista exemplos de cadeias de caracteres de associação.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-116">The following table lists examples of binding strings.</span></span>



| <span data-ttu-id="9b7ac-117">Exemplo de ADsPath LDAP</span><span class="sxs-lookup"><span data-stu-id="9b7ac-117">LDAP ADsPath example</span></span>                                      | <span data-ttu-id="9b7ac-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b7ac-118">Description</span></span>                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9b7ac-119">LDAP</span><span class="sxs-lookup"><span data-stu-id="9b7ac-119">LDAP:</span></span>                                                     | <span data-ttu-id="9b7ac-120">Associar à raiz do namespace LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-120">Bind to the root of the LDAP namespace.</span></span>                    |
| <span data-ttu-id="9b7ac-121">LDAP://server01</span><span class="sxs-lookup"><span data-stu-id="9b7ac-121">LDAP://server01</span></span>                                           | <span data-ttu-id="9b7ac-122">Associar a um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-122">Bind to a specific server.</span></span>                                 |
| <span data-ttu-id="9b7ac-123">LDAP://server01:390</span><span class="sxs-lookup"><span data-stu-id="9b7ac-123">LDAP://server01:390</span></span>                                       | <span data-ttu-id="9b7ac-124">Associar a um servidor específico usando o número da porta especificada.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-124">Bind to a specific server using the specified port number.</span></span> |
| <span data-ttu-id="9b7ac-125">LDAP:Binding = Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="9b7ac-125">LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span>          | <span data-ttu-id="9b7ac-126">Associar a um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-126">Bind to a specific object.</span></span>                                 |
| <span data-ttu-id="9b7ac-127">LDAP://server01/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="9b7ac-127">LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com</span></span> | <span data-ttu-id="9b7ac-128">Associar a um objeto específico por meio de um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-128">Bind to a specific object through a specific server.</span></span>       |



 

<span data-ttu-id="9b7ac-129">Se a autenticação Kerberos for necessária para a conclusão bem-sucedida de uma solicitação de diretório específica, a cadeia de vinculação deverá usar um ADsPath sem servidor, como LDAP:Binding = Jeff Smith, CN = Users, DC = Fabrikam, DC = com ou deve usar um ADsPath com um nome de servidor DNS totalmente qualificado, como LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-129">If Kerberos authentication is required for the successful completion of a specific directory request, the binding string must use either a serverless ADsPath, such as LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, or it must use an ADsPath with a fully qualified DNS server name, such as LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com.</span></span> <span data-ttu-id="9b7ac-130">A associação ao servidor usando um nome NETBIOS simples ou um nome DNS curto, por exemplo, usando o nome Server01 em vez de server01.fabrikam.com, não é garantida para produzir a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-130">Binding to the server using a flat NETBIOS name or a short DNS name, for example, using the name server01 instead of server01.fabrikam.com, is not guaranteed to yield Kerberos authentication.</span></span>

<span data-ttu-id="9b7ac-131">Para obter mais informações e exemplos de cadeias de vinculação LDAP, bem como uma descrição de caracteres especiais que podem ser usados em cadeias de vinculação LDAP, consulte ADsPath LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-131">For more information and examples of LDAP binding strings, as well as a description of special characters that can be used in LDAP binding strings, see LDAP ADsPath.</span></span>

<span data-ttu-id="9b7ac-132">**Windows 2000 com SP1 e posterior:** Com o provedor LDAP, se uma cadeia de vinculação incluir um nome de servidor, você poderá aumentar o desempenho usando o sinalizador de **\_ \_ associação do servidor ADS** com a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="9b7ac-132">**Windows 2000 with SP1 and later:** With the LDAP provider, if a binding string includes a server name, you can increase performance by using the **ADS\_SERVER\_BIND** flag with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="9b7ac-133">O sinalizador de **\_ \_ ligação do servidor ADS** indica que um nome de servidor foi especificado, o que permite que a ADSI Evite tráfego de rede adicional e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-133">The **ADS\_SERVER\_BIND** flag indicates that a server name was specified, which enables ADSI to avoid additional, unnecessary network traffic.</span></span>

## <a name="ldap-special-characters"></a><span data-ttu-id="9b7ac-134">Caracteres especiais do LDAP</span><span class="sxs-lookup"><span data-stu-id="9b7ac-134">LDAP Special Characters</span></span>

<span data-ttu-id="9b7ac-135">O LDAP tem vários caracteres especiais que são reservados para uso pela API LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-135">LDAP has several special characters which are reserved for use by the LDAP API.</span></span> <span data-ttu-id="9b7ac-136">A lista de caracteres especiais pode ser encontrada em [nomes distintos](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="9b7ac-136">The list of special characters can be found in [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span> <span data-ttu-id="9b7ac-137">Para usar um desses caracteres em um ADsPath sem gerar um erro, o caractere deve ser precedido por um caractere de barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9b7ac-137">To use one of these characters in an ADsPath without generating an error, the character must be preceded by a backslash (\\) character.</span></span> <span data-ttu-id="9b7ac-138">Isso é conhecido como *escapar* do caractere.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-138">This is known as *escaping* the character.</span></span> <span data-ttu-id="9b7ac-139">Por exemplo, se um nome de usuário for fornecido na forma de " <last name> , <first name> ", a vírgula no valor de nome deverá ter escape.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-139">For example, if a user name is given in the form of "<last name>,<first name>", the comma in the name value must be escaped.</span></span> <span data-ttu-id="9b7ac-140">A cadeia de caracteres resultante ficaria assim:</span><span class="sxs-lookup"><span data-stu-id="9b7ac-140">The resulting string would look like this:</span></span>


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="9b7ac-141">O caractere de escape também pode ser especificado por seu código de caractere hexadecimal de dois dígitos.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-141">The escaped character can also be specified by its two digit hexadecimal character code.</span></span> <span data-ttu-id="9b7ac-142">Isso é mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-142">This is shown in the following example.</span></span>


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



<span data-ttu-id="9b7ac-143">Os caracteres não imprimíveis, como a alimentação de linha e o retorno de carro, devem ser inseridos e especificados pelo código de caractere hexadecimal de dois dígitos.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-143">Non-printable characters, such as the line feed and carriage return, must be escaped and specified by their two digit hexadecimal character code.</span></span> <span data-ttu-id="9b7ac-144">Isso é mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b7ac-144">This is shown in the following example.</span></span>


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a><span data-ttu-id="9b7ac-145">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="9b7ac-145">For More Information</span></span>

<span data-ttu-id="9b7ac-146">Para obter mais informações sobre a notação de nome distinto usada por serviços de diretório compatíveis com LDAP, consulte [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .</span><span class="sxs-lookup"><span data-stu-id="9b7ac-146">For more information about the distinguished name notation used by LDAP-compliant directory services, see [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt).</span></span>

 

 