---
description: Explica como os serviços de certificados processam solicitações de certificado.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Processando solicitações de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567929"
---
# <a name="processing-certificate-requests"></a>Processando solicitações de certificado

Os serviços de certificados executam as seguintes etapas ao processar uma [*solicitação de certificado*](../secgloss/c-gly.md):

1.  Solicitar recebimento.

    A [*solicitação de certificado*](../secgloss/c-gly.md) é enviada pelo cliente para um aplicativo intermediário, que o formata em uma \# solicitação de formato PKCS 10 e a envia para o mecanismo do servidor.

2.  Solicitar aprovação.

    O mecanismo de servidor chama o [módulo de política](policy-modules.md), que consulta as propriedades da solicitação, decide se a solicitação está autorizada ou não e define as propriedades opcionais do certificado.

3.  Formação do certificado.

    Se a solicitação for aprovada, o mecanismo do servidor usará a solicitação e todas as propriedades solicitadas pelo módulo de política e criará um certificado completo.

4.  Publicação de certificado.

    O mecanismo de servidor armazena o certificado concluído no banco de dados de serviços de certificados e notifica o aplicativo intermediário do status da solicitação. Se o [módulo de saída](exit-modules.md) tiver sido solicitado, o mecanismo do servidor irá notificá-lo de um evento de emissão de certificado. Isso permite que o módulo de saída execute outras operações, como publicar o certificado em um repositório de certificado externo (por exemplo, um serviço de diretório). Enquanto isso, o intermediário Obtém o certificado publicado dos serviços de certificados e o passa de volta para o cliente.

A ilustração a seguir mostra como uma [*solicitação de certificado*](../secgloss/c-gly.md) é processada pelos serviços de certificados.

![processando uma solicitação de certificado](images/certflow.png)

 

 
