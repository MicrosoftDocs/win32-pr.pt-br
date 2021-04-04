---
title: Funções de serviço de diretório (AD DS)
description: As funções de serviço de diretório fornecem um utilitário para localizar um controlador de domínio (DC) em um domínio do Windows NT ou do Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Funções de serviço de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104007003"
---
# <a name="directory-service-functions-ad-ds"></a>Funções de serviço de diretório (AD DS)

As funções de serviço de diretório fornecem um utilitário para localizar um controlador de domínio (DC) em um domínio do Windows NT ou do Windows 2000. A arquitetura interage com clientes, bem como com servidores em todas as versões do Windows NT e do Windows 2000. As funções a seguir permitem que os desenvolvedores trabalhem com o controlador de domínio e a associação de domínio no serviço de diretório:

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

O localizador de DC, [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea), é implementado pelo serviço Netlogon. Cada DC registra seu nome DNS no servidor DNS e seu nome NetBIOS usando um mecanismo específico de transporte, por exemplo, no WINS. O localizador de DC pesquisa o nome e, em seguida, envia um datagrama para, ou pings, o DC que registrou o nome. Para nomes de domínio NetBIOS, o datagrama é uma mensagem do processador de mensagens. Para nomes de domínio DNS, o datagrama é uma pesquisa LDAP UDP. Cada DC responde indicando que ele está operacional no momento. O primeiro DC a responder é retornado ao chamador.

O DC retornado é armazenado em cache, para que os chamadores subsequentes não precisem repetir o algoritmo anterior e para encorajar todos os chamadores a usarem o mesmo DC. Isso garante que um único cliente tenha uma exibição consistente do conteúdo do controlador de domínio.

Ao procurar um DC pelo nome de domínio DNS, o localizador de DC tenta encontrar um DC no site "mais próximo". Cada DC registra registros DNS adicionais que indicam em qual site o controlador de domínio está e quais sites o DC inclui. O localizador de DC procura primeiro esse registro DNS específico do site antes de Pesquisar o registro DNS que não seja específico do site, preferindo assim um controlador de domínio nesse site. Quando o localizador de DC envia um datagrama para o DC, o DC procura o endereço IP do cliente no contêiner de configuração/sites/sub-rede do DS para localizar um objeto de sub-rede. A propriedade **siteobject** do objeto subnet define o nome do site que contém o cliente. O DC responde ao ping com o nome do site que contém o cliente, juntamente com um indicador de se esse controlador de domínio cobre esse site. Se o controlador de domínio não incluir esse site e o localizador de DC ainda não tiver tentado localizar um controlador de domínio nesse site, o localizador de DC tentará novamente localizar um controlador de domínio no site.

Para localizar o nome do site que contém o cliente, use a função [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . Os nomes dos objetos no contêiner de configuração/sites/sub-rede devem ser nomes de sub-rede válidos. A função [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) indica se um nome de sub-rede especificado é válido.

 

 




