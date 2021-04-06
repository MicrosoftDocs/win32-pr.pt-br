---
title: Associação com criptografia
description: Dados confidenciais trocados em uma rede devem ser criptografados.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associação com criptografia
- Associação com criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915912"
---
# <a name="binding-with-encryption"></a>Associação com criptografia

Dados confidenciais trocados em uma rede devem ser criptografados. Para permitir isso, a ADSI dá suporte a dois tipos de criptografia, Kerberos e protocolo SSL (SSL). Os dois tipos de criptografia exigem o uso de [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para associação.

**GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) não podem ser usados para associação nesse caso porque essas funções causam as solicitações LDAP usadas pela ADSI e os dados retornados do servidor de diretório para transmitir pela rede como texto sem formatação. Para fins de depuração, é útil desativar a criptografia para que a Monitor de Rede possa ser usada para exibir as solicitações LDAP e os dados entre o cliente e o servidor de diretório.

## <a name="kerberos-based-encryption"></a>Criptografia baseada em Kerberos

Para usar a criptografia baseada em Kerberos, especifique os **anúncios usar sinalizador de \_ \_ lacre** ao chamar [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Os **anúncios \_ usam \_** o sinalizador de lacre também podem ser usados para verificar a integridade dos dados, ou seja, para garantir que os dados recebidos sejam os mesmos que os dados enviados. Se o sinalizador **ADS \_ use \_ lacre** for especificado, o sinalizador de uso de **\_ \_ assinatura do ADS** também será especificado automaticamente. Ambos os sinalizadores exigem autenticação Kerberos, que funciona somente sob as seguintes condições:

-   O computador cliente deve estar conectado ao domínio do Windows ou a um domínio confiável para um domínio do Windows.
-   [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) deve ser chamado com credenciais nulas; ou seja, as credenciais alternativas não podem ser especificadas.

## <a name="ssl-based-encryption"></a>Criptografia baseada em SSL

Para usar a criptografia baseada em SSL, especifique o sinalizador de **\_ uso de \_ SSL do ADS** ao chamar [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Se apenas o sinalizador de **\_ uso de \_ SSL do ADS** for especificado, a ADSI abrirá a porta SSL 636 e, em seguida, executará uma associação simples nesse canal SSL. Se os anúncios **de \_ \_ autenticação segura** e os **ADS \_ usarem sinalizadores \_ SSL** forem especificados, o comportamento de associação dependerá do cliente do qual a chamada é feita. Em versões sem suporte do Windows, a ADSI primeiro abriu um canal SSL e executa uma associação simples usando o nome de usuário e a senha especificados ou o contexto de usuário atual, se o nome de usuário e a senha forem nulos. Nas versões com suporte do Windows, a ADSI executa uma autenticação segura em vez de uma associação simples.

Para usar a criptografia baseada em SSL ao se comunicar com o Active Directory, Active Directory deve ter a PKI (infraestrutura de chave pública) habilitada. A PKI pode ser habilitada Configurando uma autoridade de certificação corporativa em um dos servidores no Active Directory, incluindo um dos servidores Active Directory em si. Configurar uma autoridade de certificação corporativa faz com que um servidor de Active Directory obtenha um certificado de servidor que pode ser usado para fazer a criptografia baseada em SSL.

 

 




