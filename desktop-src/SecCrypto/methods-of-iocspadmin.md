---
description: Os métodos a seguir são definidos pela interface IOCSPAdmin. Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de IOCSPAdmin, consulte Propriedades de IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Métodos de IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296418"
---
# <a name="methods-of-iocspadmin"></a>Métodos de IOCSPAdmin

Os métodos a seguir são definidos pela interface [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) . Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de **IOCSPAdmin**, consulte [Propriedades de IOCSPAdmin](properties-of-iocspadmin.md).



| Método                                                              | Descrição                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Conecta-se a um servidor de respondente OCSP (protocolo de status de certificado online) e inicializa um objeto **OCSPAdmin** com as informações de configuração do servidor.                                                                                                     |
| [**Gethashalgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Obtém uma lista de nomes de algoritmos de hash. O servidor Respondente usa um dos algoritmos nomeados para assinar respostas OCSP para uma determinada configuração de [*autoridade de certificação*](../secgloss/c-gly.md) (CA). |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Obtém a máscara de acesso das funções de privilégio para um usuário em um determinado servidor de respondente.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Obtém informações do descritor de segurança para um servidor respondente.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Obtém os certificados de autenticação que estão disponíveis em um servidor Respondente para um determinado certificado de autoridade de certificação.                                                                                                                                                                        |
| [**Executar**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Testa uma conexão DCOM com um serviço Respondente.                                                                                                                                                                                                                         |
| [**Configuração de**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Atualiza um serviço Respondente com alterações de configuração.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Atualiza as informações do descritor de segurança de um servidor de respondente OCSP.                                                                                                                                                                                                     |



 

 

 
