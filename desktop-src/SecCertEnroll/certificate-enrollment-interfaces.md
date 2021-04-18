---
description: As interfaces a seguir podem ser usadas para registrar um usuário ou um computador em uma hierarquia de certificado.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760213"
---
# <a name="certificate-enrollment-interfaces"></a>Interfaces de registro de certificado

As interfaces a seguir podem ser usadas para registrar um usuário ou um computador em uma hierarquia de certificado.



| Interface                                              | Descrição                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Registra um computador ou usuário em uma hierarquia de certificado.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Estende a interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para habilitar a inicialização a partir de um modelo.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Define métodos que permitem que um aplicativo Web registre um certificado, armazene as credenciais do servidor de política no cache de credenciais e registre servidores de política e servidores de registro. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Recupera informações detalhadas de erro sobre uma transação de registro de certificado.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Interface de protocolo de registro de computador simples X. 509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 




