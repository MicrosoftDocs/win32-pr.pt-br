---
description: Os arquivos de configuração de grupo e de identidade de par podem ser importados e exportados de um ponto de extremidade para outro usando as funções de importação e exportação de identidade localizadas no Gerenciador de identidades e APIs de agrupamento.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importação e exportação de configuração de grupo e identidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662189"
---
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="3e4fc-103">Importação e exportação de configuração de grupo e identidade</span><span class="sxs-lookup"><span data-stu-id="3e4fc-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="3e4fc-104">Os arquivos de configuração de grupo e de identidade de par podem ser importados e exportados de um ponto de extremidade para outro usando as funções de importação e exportação de identidade localizadas no Gerenciador de identidades e APIs de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="3e4fc-105">Essas funções são úteis porque permitem que um usuário exporte de forma rápida e conveniente as identidades e as informações de configuração de um computador para outro.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="3e4fc-106">Importando e exportando dados de identidade de pares</span><span class="sxs-lookup"><span data-stu-id="3e4fc-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="3e4fc-107">Os dados de identidade de um par são exportados chamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) com o nome de identidade a ser exportado e uma senha usada para criptografar as credenciais associadas.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="3e4fc-108">Essa função retorna uma cadeia de caracteres XML que contém o nome da identidade do par e as credenciais criptografadas para essa identidade específica, que podem ser passadas para um computador diferente usando um mecanismo de transferência externo, como email.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="3e4fc-109">O exemplo a seguir mostra o formato da cadeia de caracteres XML:</span><span class="sxs-lookup"><span data-stu-id="3e4fc-109">The following example shows you the format of the XML string:</span></span>

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

<span data-ttu-id="3e4fc-110">Os dados de identidade exportados podem ser recuperados chamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando a cadeia de caracteres XML com a senha fornecida na chamada anterior para [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span><span class="sxs-lookup"><span data-stu-id="3e4fc-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="3e4fc-111">Essa função retorna o nome do par da identidade importada.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="3e4fc-112">O nome de identidade e as credenciais importados podem ser usados exatamente como um nome de identidade retornado por [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) ou [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span><span class="sxs-lookup"><span data-stu-id="3e4fc-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="3e4fc-113">Ao chamar [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), o aplicativo ou usuário de API deve fornecer uma senha forte de comprimento suficiente.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="3e4fc-114">Isso é importante porque os dados de identidade importados contêm a chave privada para a identidade.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="3e4fc-115">Importando e exportando uma configuração de identidade de grupo</span><span class="sxs-lookup"><span data-stu-id="3e4fc-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="3e4fc-116">O agrupamento de pares permite que um par exporte dados de configuração de grupo de um ponto de extremidade para outro usando APIs específicas de importação e exportação.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="3e4fc-117">Para importar dados de configuração, a identidade do par que está executando a importação (e quem realizou a exportação anteriormente) deve estar presente no computador onde os dados de configuração devem ser importados.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="3e4fc-118">Essa identidade pode ser obtida exportando-a e importando-a pelos métodos especificados na seção anterior deste tópico: [importando e exportando dados de identidade de pares](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="3e4fc-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="3e4fc-119">Os dados de configuração de grupo contêm todas as informações de uma identidade para ingressar em um grupo de um novo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="3e4fc-120">Especificamente, os dados de configuração contêm a cadeia GMC, o nome do par do grupo, o nome da nuvem, o escopo e um conjunto de sinalizadores específicos de PNRP.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="3e4fc-121">Para uma identidade que possui um grupo, uma chave privada para o grupo é incluída nas informações de configuração do grupo.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="3e4fc-122">Ao chamar [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), um usuário de aplicativo ou API deve fornecer uma senha forte de comprimento suficiente.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="3e4fc-123">Isso é importante porque os dados de identidade importados contêm a chave privada para o grupo.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="3e4fc-124">Para exportar a configuração atual do grupo de pares, chame [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando o identificador para o grupo (obtido por uma chamada anterior para [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)ou [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) e uma senha usada para criptografar e proteger o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="3e4fc-125">Essa função retorna uma cadeia de caracteres XML que contém a configuração no formato do exemplo a seguir, que pode ser gravada em um arquivo e transmitida para outro computador usando um mecanismo de transferência externo, como email.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

<span data-ttu-id="3e4fc-126">Depois de obter a configuração de grupo como uma cadeia de caracteres XML, o grupo pode ser importado chamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) com a cadeia de caracteres XML de configuração e a senha específica fornecida para [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span><span class="sxs-lookup"><span data-stu-id="3e4fc-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="3e4fc-127">Essa função retorna um nome de identidade e um nome de par de grupo, que pode ser fornecido para [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e uma conexão com o grupo estabelecido.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



