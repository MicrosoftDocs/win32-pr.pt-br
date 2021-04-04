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
# <a name="identity-and-group-configuration-import-and-export"></a>Importação e exportação de configuração de grupo e identidade

Os arquivos de configuração de grupo e de identidade de par podem ser importados e exportados de um ponto de extremidade para outro usando as funções de importação e exportação de identidade localizadas no Gerenciador de identidades e APIs de agrupamento. Essas funções são úteis porque permitem que um usuário exporte de forma rápida e conveniente as identidades e as informações de configuração de um computador para outro.

## <a name="importing-and-exporting-peer-identity-data"></a>Importando e exportando dados de identidade de pares

Os dados de identidade de um par são exportados chamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) com o nome de identidade a ser exportado e uma senha usada para criptografar as credenciais associadas. Essa função retorna uma cadeia de caracteres XML que contém o nome da identidade do par e as credenciais criptografadas para essa identidade específica, que podem ser passadas para um computador diferente usando um mecanismo de transferência externo, como email. O exemplo a seguir mostra o formato da cadeia de caracteres XML:

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

Os dados de identidade exportados podem ser recuperados chamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando a cadeia de caracteres XML com a senha fornecida na chamada anterior para [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Essa função retorna o nome do par da identidade importada. O nome de identidade e as credenciais importados podem ser usados exatamente como um nome de identidade retornado por [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) ou [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

> [!Note]  
> Ao chamar [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), o aplicativo ou usuário de API deve fornecer uma senha forte de comprimento suficiente. Isso é importante porque os dados de identidade importados contêm a chave privada para a identidade.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importando e exportando uma configuração de identidade de grupo

O agrupamento de pares permite que um par exporte dados de configuração de grupo de um ponto de extremidade para outro usando APIs específicas de importação e exportação. Para importar dados de configuração, a identidade do par que está executando a importação (e quem realizou a exportação anteriormente) deve estar presente no computador onde os dados de configuração devem ser importados. Essa identidade pode ser obtida exportando-a e importando-a pelos métodos especificados na seção anterior deste tópico: [importando e exportando dados de identidade de pares](#importing-and-exporting-peer-identity-data).

Os dados de configuração de grupo contêm todas as informações de uma identidade para ingressar em um grupo de um novo ponto de extremidade. Especificamente, os dados de configuração contêm a cadeia GMC, o nome do par do grupo, o nome da nuvem, o escopo e um conjunto de sinalizadores específicos de PNRP. Para uma identidade que possui um grupo, uma chave privada para o grupo é incluída nas informações de configuração do grupo.

> [!Note]  
> Ao chamar [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), um usuário de aplicativo ou API deve fornecer uma senha forte de comprimento suficiente. Isso é importante porque os dados de identidade importados contêm a chave privada para o grupo.

 

Para exportar a configuração atual do grupo de pares, chame [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando o identificador para o grupo (obtido por uma chamada anterior para [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)ou [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) e uma senha usada para criptografar e proteger o arquivo de configuração. Essa função retorna uma cadeia de caracteres XML que contém a configuração no formato do exemplo a seguir, que pode ser gravada em um arquivo e transmitida para outro computador usando um mecanismo de transferência externo, como email.

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

Depois de obter a configuração de grupo como uma cadeia de caracteres XML, o grupo pode ser importado chamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) com a cadeia de caracteres XML de configuração e a senha específica fornecida para [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig). Essa função retorna um nome de identidade e um nome de par de grupo, que pode ser fornecido para [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e uma conexão com o grupo estabelecido.

 

 



