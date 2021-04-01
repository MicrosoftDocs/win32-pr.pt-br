---
description: As interfaces a seguir podem ser usadas para criar uma propriedade de certificado.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfaces de propriedade de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d0052675436a28438d5f1600a5b0097f8e177a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646669"
---
# <a name="certificate-property-interfaces"></a>Interfaces de propriedade de certificado

As interfaces a seguir podem ser usadas para criar uma propriedade de certificado.



| Interface                                                                          | Descrição                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Gerenciar uma coleção de objetos [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) .                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Associa uma propriedade externa a um certificado.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Representa uma propriedade de certificado que identifica se um certificado foi arquivado.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Representa um hash SHA-1 de uma chave privada criptografada enviada a uma autoridade de certificação para arquivamento.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Representa uma propriedade de certificado que identifica um modelo que foi configurado para habilitar o registro automático do certificado.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Representa uma propriedade de certificado que identifica se foi feito o backup de um certificado e, em caso afirmativo, a data e hora em que ele foi salvo.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Permite especificar e recuperar uma cadeia de caracteres que contém informações descritivas de um certificado.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Representa uma propriedade de certificado que contém informações de certificado e autoridade de certificação criadas quando o cliente chama o método de [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) na interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Representa uma propriedade de certificado externo que contém informações sobre um servidor de política de registro de certificado (CEP) e um servidor de registro de certificado (CES).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Permite especificar e recuperar uma cadeia de caracteres que contém o nome de exibição de um certificado.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Representa uma propriedade de certificado que contém informações sobre uma chave privada.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Representa uma propriedade de certificado que contém um hash SHA-1 do novo certificado criado quando um certificado existente é renovado.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa uma propriedade de certificado que contém o nome DNS (sistema de nomeação de domínio) do computador no qual a solicitação foi criada.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa uma propriedade de certificado que contém o nome DNS (sistema de nomeação de domínio) do computador no qual a solicitação foi criada.                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



