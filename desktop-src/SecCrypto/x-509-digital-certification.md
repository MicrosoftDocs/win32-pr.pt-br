---
description: A certificação digital envolve um processo para assinar o certificado. Esse processo é descrito.
ms.assetid: bb0382fd-2924-429f-933b-84ab61debf20
title: Certificação Digital X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2f737a658e3e2c44876a23206f23a3d45ff3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169683"
---
# <a name="x509-digital-certification"></a>Certificação Digital X.509

Uma tarefa principal de um [*certificado digital*](../secgloss/d-gly.md) é fornecer acesso à [*chave pública*](../secgloss/p-gly.md)da entidade. O certificado também confirma que a chave pública do certificado pertence à entidade do certificado. Por exemplo, uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA) pode assinar digitalmente uma mensagem especial (as informações do certificado) que contém o nome de algum usuário, digamos "Alice" e sua chave pública. Isso deve ser feito de forma que qualquer pessoa possa verificar se o certificado foi emitido e assinado por um que não seja a autoridade de certificação. Se a CA é confiável e pode ser verificada que o certificado de Alice foi emitido por essa CA, qualquer destinatário do certificado de Alice pode confiar na chave pública de Alice desse certificado.

A implementação típica da certificação digital envolve um processo para assinar o certificado.

O processo é assim:

1.  Alice envia uma [*solicitação de certificado*](../secgloss/c-gly.md) assinada contendo seu nome, sua chave pública e, talvez, algumas informações adicionais para uma CA.
2.  A CA cria uma mensagem, *m*, da solicitação de Alice. A CA assina a mensagem com sua chave privada, criando uma mensagem de assinatura separada, *SIG*. A CA retorna a mensagem, *m*, e a assinatura, *SIG*, para Alice. Em conjunto, *m* e *SIG* o certificado de Alice do formulário.
3.  Alice envia as duas partes de seu certificado para Bob para dar acesso à sua chave pública.
4.  Bob verifica a assinatura, *SIG* usando a chave pública da autoridade de certificação. Se a assinatura provar válida, ele aceitará a chave pública no certificado como a chave pública de Alice.

Assim como ocorre com qualquer [*assinatura digital*](../secgloss/d-gly.md), qualquer destinatário com acesso à chave pública da autoridade de certificação pode determinar se uma autoridade de certificação específica assinou o certificado. Esse processo não requer acesso a nenhuma informação secreta. O cenário que acabamos de ver pressupõe que Bob tem acesso à chave pública da autoridade de certificação. Bob teria acesso a essa chave se ele tiver uma cópia do certificado da autoridade de certificação que contém essa chave pública.

Os certificados digitais [*X. 509*](../secgloss/x-gly.md) incluem não apenas o nome e a chave pública de um usuário, mas também outras informações sobre o usuário. Esses certificados são mais do que a etapa em uma hierarquia digital de confiança. Eles permitem que a autoridade de certificação dê ao receptor do certificado um meio de confiar não apenas na chave pública do assunto do certificado, mas também por outras informações sobre o assunto do certificado. Essas outras informações podem incluir, entre outras coisas, um endereço de email, uma autorização para assinar documentos de um determinado valor ou a autorização para se tornar uma CA e assinar outros certificados.

Os certificados X. 509 e muitos outros certificados têm uma duração de tempo válida. Um certificado pode expirar e não ser mais válido. Uma autoridade de certificação pode revogar um certificado por vários motivos. Para lidar com as revogações, uma CA mantém e distribui uma lista de certificados revogados chamada CRL ( [*lista de certificados*](../secgloss/c-gly.md) revogados). Os usuários de rede acessam a CRL para determinar a validade de um certificado.

 

 
