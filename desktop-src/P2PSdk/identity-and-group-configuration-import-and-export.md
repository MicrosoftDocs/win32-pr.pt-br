---
description: Arquivos de configuração de grupo e identidade de par podem ser importados e exportados de um ponto de extremidade para outro usando as funções de importação e exportação de identidade localizadas nas APIs do Identity Manager e do Grouping.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importação e exportação de configuração de identidade e grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0102bda821b7157edc512aeea4a8e315c0dbfa1def85f9a61919ec0f2c86da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519326"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importação e exportação de configuração de identidade e grupo

Arquivos de configuração de grupo e identidade de par podem ser importados e exportados de um ponto de extremidade para outro usando as funções de importação e exportação de identidade localizadas nas APIs do Identity Manager e do Grouping. Essas funções são úteis porque permitem que um usuário exporte de maneira rápida e conveniente identidades e informações de configuração de grupo de um computador para outro.

## <a name="importing-and-exporting-peer-identity-data"></a>Importando e exportando dados de identidade de par

Os dados de identidade de um par são exportados chamando [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) com o nome de identidade a ser exportado e uma senha usada para criptografar as credenciais associadas. Essa função retorna uma cadeia de caracteres XML que contém o nome de identidade do par e as credenciais criptografadas para essa identidade específica, que pode ser passada para um computador diferente usando um mecanismo de transferência externa, como email. O exemplo a seguir mostra o formato da cadeia de caracteres XML:

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

Os dados de identidade exportados podem ser recuperados chamando [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)e passando a cadeia de caracteres XML com a senha fornecida na chamada anterior para [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport). Essa função retorna o nome par da identidade importada. O nome de identidade importado e as credenciais podem ser usados como um nome de identidade retornado por [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) ou [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

> [!Note]  
> Ao chamar [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), o aplicativo ou o usuário da API deve fornecer uma senha forte de comprimento suficiente. Isso é importante porque os dados de identidade importados contêm a chave privada para a identidade.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importando e exportando uma configuração de identidade de grupo

O Grupo de Pares permite que um par exporte dados de configuração de grupo de um ponto de extremidade para outro usando APIs de importação e exportação específicas. Para importar dados de configuração, a identidade do par que executa a importação (e quem realizou a exportação anteriormente) deve estar presente no computador em que os dados de configuração devem ser importados. Essa identidade pode ser obtida exportando e importando-a pelos métodos especificados na seção anterior deste tópico: Importando e [exportando](#importing-and-exporting-peer-identity-data)dados de identidade par.

Os dados de configuração de grupo contêm todas as informações de uma identidade para ingressar em um grupo de um novo ponto de extremidade. Especificamente, os dados de configuração contêm a cadeia do GMC, o nome do par de grupo, o nome da nuvem, o escopo e um conjunto de sinalizadores específicos do PNRP. Para uma identidade que possui um grupo, uma chave privada para o grupo é incluída nas informações de configuração do grupo.

> [!Note]  
> Ao chamar [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), um usuário de aplicativo ou API deve fornecer uma senha forte de comprimento suficiente. Isso é importante porque os dados de identidade importados contêm a chave privada para o grupo.

 

Para exportar a configuração de grupo par atual, chame [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passando o handle para o grupo (obtido por uma chamada anterior para [**PeerGroupJoin,**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)ou [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)) e uma senha usada para criptografar e proteger o arquivo de configuração. Essa função retorna uma cadeia de caracteres XML que contém a configuração no formato do exemplo a seguir, que pode ser gravado em um arquivo e passado para outro computador usando um mecanismo de transferência externa, como email.

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

Depois de obter a configuração de grupo como uma cadeia de caracteres XML, o grupo pode ser importado chamando [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) com a cadeia de caracteres XML de configuração e a senha específica fornecida para [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig). Essa função retorna um nome de identidade e um nome par de grupo, que pode ser fornecido para [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e uma conexão com o grupo estabelecido.

 

 



