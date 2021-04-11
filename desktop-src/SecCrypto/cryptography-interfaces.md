---
description: Lista as interfaces fornecidas pelo CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfaces de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5284f5c2107e741fd91e2936ff3dea0853e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296275"
---
# <a name="cryptography-interfaces"></a>Interfaces de criptografia

As interfaces de criptografia são categorizadas de acordo com o uso da seguinte maneira:

-   [Interfaces de exportação do mecanismo do servidor](#server-engine-export-interfaces)
-   [Interfaces de importação do mecanismo do servidor](#server-engine-import-interfaces)
-   [Interfaces de codificação](#encoding-interfaces)
-   [Interfaces de registro de certificado](#certificate-enrollment-interfaces)
-   [Interfaces de interoperabilidade CAPICOM](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfaces de exportação do mecanismo do servidor

O tópico de referência a seguir descreve as interfaces exportadas pelo mecanismo de servidor e são chamadas por objetos externos.



| Interface                                                                | Descrição                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Usado por programas de administração para gerenciar solicitações, certificados e revogações.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Usado por programas de administração para gerenciar solicitações, certificados e revogações. Substitui [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Usado pelos clientes para obter informações sobre os servidores disponíveis.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Usado pelos clientes para obter informações sobre os servidores disponíveis. Substitui [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Fornece a funcionalidade para recuperar os dados de configuração pública (especificados durante a configuração do cliente) para um servidor de [*serviços de certificados*](../secgloss/c-gly.md) .                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Usado para enviar uma solicitação ao servidor e obter os resultados da solicitação.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Usado para enviar uma solicitação ao servidor e obter os resultados da solicitação. Substitui [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Usado por [módulos de saída](exit-modules.md) para obter as propriedades de certificado e de solicitação.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Usado pelo [módulo de política](policy-modules.md) para obter e definir as propriedades de certificado e de solicitação.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Usado por clientes para [Exibir o banco de dados dos serviços de certificados](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Usado por clientes para exibir o banco de dados dos serviços de certificados. Substitui [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Usado pelos clientes para acessar os atributos de certificado para uma linha na exibição de serviços de certificados.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Usado pelos clientes para acessar as colunas de dados de uma linha no modo de exibição serviços de certificados.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Usado por clientes para acessar os dados de extensão de certificado para uma linha na exibição de serviços de certificados.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Usado pelos clientes para enumerar as linhas do modo de exibição de serviços de certificados.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Usado por programas de administração para configurar servidores respondentes do protocolo OCSP.                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Fornece a funcionalidade para configurar um serviço de respondente OCSP para lidar com solicitações de status para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA) específica.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Fornece a funcionalidade para gerenciar as configurações de autoridade de certificação para as quais um serviço de respondente OCSP pode manipular solicitações.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Fornece a funcionalidade para configurar um atributo de servidor de respondente OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Usado por programas de administração para gerenciar atributos de servidor de respondente OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfaces de importação do mecanismo do servidor

Os tópicos de referência a seguir descrevem as interfaces que são importadas pelo mecanismo do servidor.



| Interface                                      | Descrição                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Exportado por módulos de saída. Usado pelo mecanismo do servidor para fornecer certificados concluídos e informações de revogação.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Adiciona o método [**GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) a [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit).                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Exportado por módulos de política ou de saída. Usado para exibir informações do módulo ou para exibir uma interface do usuário para a configuração do módulo. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Exportado pelo módulo de política. Usado pelo mecanismo de servidor para verificar solicitações e obter propriedades de certificados.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Adiciona o método [**GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy).                         |



 

## <a name="encoding-interfaces"></a>Interfaces de codificação

Os tópicos de referência a seguir descrevem as interfaces que podem ser exportadas por [manipuladores de extensão](writing-custom-extension-handlers.md) e são importadas pelo módulo de política.



| Interface                                                | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Usado pelo [módulo de política](policy-modules.md) para lidar com extensões de nome alternativo.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Usado pelo módulo de política para manipular cadeias de caracteres de bits usadas em extensões de certificado.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Usado pelo módulo de política para manipular as matrizes de informações de distribuição da CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) usadas em extensões de certificado. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Usado pelo módulo de política para manipular matrizes de **Data** usadas em extensões de certificado.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Usado pelo módulo de política para lidar com matrizes **longas** usadas em extensões de certificado.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Usado pelo módulo de política para tratar matrizes de **cadeias de caracteres** usadas em extensões de certificado.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfaces de registro de certificado

Esta seção descreve os objetos, métodos e propriedades do controle de registro de certificado e o objeto, os métodos e as propriedades disponíveis no controle de registro de cartão inteligente. Elas incluem as seguintes interfaces.



| Interface                                                                                  | Descrição                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Uma das várias interfaces que representam o controle de registro de certificado. Se você não estiver usando a automação, será de interesse.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Uma das várias interfaces que representam o controle de registro de certificado. Se você não estiver usando a automação, será de interesse.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Uma das várias interfaces que representam o controle de registro de certificado. Se você não estiver usando a automação, será de interesse.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Representa o serviço Web de CEP (política de registro de certificado) dentro do ADCS (serviços de certificados do Active Directory). O serviço permite que usuários e computadores obtenham informações de política de registro de certificado. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Representa o Serviço Web de Registro de Certificado (CES) em ADCS. O serviço permite que usuários e computadores se registrem e renovem certificados.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Uma das várias interfaces que representam o controle de registro de certificado. Se você não estiver usando a automação, será de interesse.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Uma das várias interfaces que representam o controle de registro de certificado. A interface é, principalmente, interessante se você não estiver usando a automação.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Uma das várias interfaces que representam o controle de registro de certificado. A interface é, principalmente, interessante se você não estiver usando a automação.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Uma das várias interfaces que representam o controle de registro de certificado. A interface é, principalmente, interessante se você não estiver usando a automação.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Representa o controle de registro de cartão inteligente. Se você não estiver usando a automação, será de interesse.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfaces de interoperabilidade CAPICOM

Os tópicos de referência a seguir descrevem as interfaces que permitem que as derivações de CryptoAPI funcionem em conjunto com o CAPICOM 2,0.



| Interface                              | Descrição                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fornece acesso ao contexto de um objeto de [**certificado**](certificate.md) CAPICOM X. 509v3. Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fornece acesso ao contexto de um objeto de [**armazenamento**](store.md) capicor. Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornece acesso ao contexto de um objeto de [**cadeia**](chain.md) capicor. Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.         |



 

 

 
