---
description: Uma AC (autoridade de certificação) é responsável por atestar a identidade de usuários, computadores e organizações.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Autoridades de certificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5f48c897c74e5f0bf7d4d3b1e21b8f89d33e72cdfa46aefe726f714fbc267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904495"
---
# <a name="certification-authorities"></a>Autoridades de certificação

Uma [*AC (autoridade*](/windows/desktop/SecGloss/c-gly) de certificação) é responsável por atestar a identidade de usuários, computadores e organizações. A AC autentica uma entidade e garante-a emitindo um certificado assinado digitalmente. A AC também pode gerenciar, revogar e renovar certificados.

Uma AC pode ser pública ou privada. Uma AC pública fornece serviços de certificação, normalmente por um valor, ao público pela Internet. Uma AC privada fornece esse serviço aos membros de uma população delimitada, como os funcionários de uma empresa ou membros de algum outro grupo privado.

Os meios pelos quais uma AC autentica um usuário final são variados e além do escopo desta documentação. No entanto, é claro que os métodos de autenticação variam de acordo com o tipo de provedor. Por exemplo, uma AC privada pode estabelecer a identidade dos usuários finais referindo-se a uma lista de grupos, como um banco de dados de funcionários ou o Active Directory. Os métodos de autenticação executados por uma AC pública geralmente são mais complexos e dependem parcialmente do nível de garantia que está sendo confirmado pelo certificado.

À medida que a população de uma PKI (infraestrutura de chave pública) cresce, pode se tornar difícil para uma única AC gerenciar efetivamente todos os certificados emitidos. A AC pode compensar autorizando outras AAs na PKI a emitir certificados. A AC inicial é chamada de raiz e as AAs que ela autoriza são chamadas subordinadas. As AIs subordinadas também podem designar suas próprias subsidiárias dentro dos limites definidos pela raiz. A estrutura resultante é chamada de hierarquia de certificado. Os certificados emitidos para CAs inferiores na hierarquia contêm certificados suficientes para rastrear um caminho de volta para a raiz. Isso é chamado de cadeia de certificados.

O termo autoridade de certificação pode se referir à organização que garante a identidade de um usuário final e o servidor usado pela organização para emitir e gerenciar certificados. Um Windows servidor pode ser configurado para atuar como um servidor de AC, e essa documentação geralmente se refere ao servidor ao usar o termo AC.

A API de Registro de Certificado interage com uma AC principalmente usando o [**objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) O [**método Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) neste objeto pode codificar automaticamente uma solicitação de certificado, enviar para a AC e instalar o certificado emitido. Você também pode usar um objeto **IX509Enrollment** inicializado para registro fora de banda ou para registro atrasado. Além disso, você pode usar o [**objeto IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) para monitorar o status do registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 
