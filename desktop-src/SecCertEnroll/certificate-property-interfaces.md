---
description: As interfaces a seguir podem ser usadas para criar uma propriedade de certificado.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfaces de propriedade do certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902602"
---
# <a name="certificate-property-interfaces"></a>Interfaces de propriedade do certificado

As interfaces a seguir podem ser usadas para criar uma propriedade de certificado.



| Interface                                                                          | Descrição                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Gerencie uma [**coleção de objetos ICertProperty.**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Associa uma propriedade externa a um certificado.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Representa uma propriedade de certificado que identifica se um certificado foi arquivado.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Representa um hash SHA-1 de uma chave privada criptografada enviada a uma autoridade de certificação para arquivamento.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Representa uma propriedade de certificado que identifica um modelo que foi configurado para habilitar o registro automático do certificado.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Representa uma propriedade de certificado que identifica se um certificado foi feito backup e, nesse caso, a data e a hora em que ele foi salvo.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Permite especificar e recuperar uma cadeia de caracteres que contém informações descritivas para um certificado.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Representa uma propriedade de certificado que contém informações de autoridade de certificação e certificado criadas quando o cliente chama o método [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) na interface [**IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Representa uma propriedade de certificado externo que contém informações sobre um servidor CEP (política de registro de certificado) e um CES (servidor de registro de certificado).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Permite especificar e recuperar uma cadeia de caracteres que contém o nome de exibição de um certificado.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Representa uma propriedade de certificado que contém informações sobre uma chave privada.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Representa uma propriedade de certificado que contém um hash SHA-1 do novo certificado criado quando um certificado existente é renovado.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa uma propriedade de certificado que contém o nome DNS (Sistema de Nomenização de Domínio) do computador no qual a solicitação foi criada.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa uma propriedade de certificado que contém o nome DNS (Sistema de Nomenização de Domínio) do computador no qual a solicitação foi criada.                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



