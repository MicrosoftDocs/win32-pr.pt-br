---
description: Uma AC (autoridade de certificação) é responsável por atestar a identidade de usuários, computadores e organizações.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Autoridades de certificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829323"
---
# <a name="certification-authorities"></a>Autoridades de certificação

Uma [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) é responsável por atestar a identidade de usuários, computadores e organizações. A AC autentica uma entidade e garante-a emitindo um certificado assinado digitalmente. A AC também pode gerenciar, revogar e renovar certificados.

Uma CA pode ser pública ou privada. Uma CA pública fornece serviços de certificação, normalmente por uma taxa, para o público pela Internet. Uma AC privada fornece esse serviço para os membros de uma população delimitada, como os funcionários de uma empresa ou membros de algum outro grupo privado.

O meio pelo qual uma autoridade de certificação autentica um usuário final é variado e está além do escopo desta documentação. No entanto, claramente, os métodos de autenticação variam de acordo com o tipo de provedor. Por exemplo, uma autoridade de certificação privada pode estabelecer a identidade dos usuários finais referindo-se a uma lista de grupos, como um banco de dados de funcionários ou Active Directory. Os métodos de autenticação executados por uma CA pública geralmente são mais complexos e dependem parcialmente do nível de garantia sendo prometido pelo certificado.

À medida que a população de uma PKI (infraestrutura de chave pública) cresce, pode ser difícil para uma única AC gerenciar efetivamente todos os certificados emitidos. A CA pode compensar ao autorizar outras CAs na PKI a emitir certificados. A autoridade de certificação inicial é chamada de raiz e as CAs que ela autoriza são chamadas de subordinadas. As CAs subordinadas também podem designar suas próprias subsidiárias dentro dos limites definidos pela raiz. A estrutura resultante é chamada de hierarquia de certificado. Os certificados emitidos para o CAs inferior na hierarquia contêm certificados suficientes para rastrear um caminho de volta para a raiz. Isso é chamado de cadeia de certificados.

O termo autoridade de certificação pode se referir à organização que comprovará a identidade de um usuário final e o servidor usado pela organização para emitir e gerenciar certificados. Um Windows Server pode ser configurado para atuar como um servidor de CA, e esta documentação geralmente se refere ao servidor ao usar o termo CA.

A API de registro de certificado interage com uma autoridade de certificação principalmente usando o objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . O método de [**registro**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) nesse objeto pode codificar automaticamente uma solicitação de certificado, enviá-la para a AC e instalar o certificado emitido. Você também pode usar um objeto **IX509Enrollment** inicializado para registro fora de banda ou para registro atrasado. Além disso, você pode usar o objeto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) para monitorar o status do registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 
