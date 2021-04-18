---
description: Os intermediários se comunicam com aplicativos cliente para permitir que eles enviem solicitações de certificado e (supondo que a solicitação resulte em um certificado emitido) para baixar o certificado emitido para o cliente.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: intermediários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105770335"
---
# <a name="intermediaries"></a>intermediários

Os intermediários se comunicam com aplicativos cliente para permitir que eles enviem [*solicitações de certificado*](../secgloss/c-gly.md)e (supondo que a solicitação resulte em um certificado emitido) para baixar o certificado emitido para o cliente. Cada protocolo de camada de transporte requer seu próprio intermediário.

Os serviços de certificados da Microsoft são fornecidos com um intermediário (as páginas de registro da Web) para HTTP. Outro exemplo de um intermediário é o snap-in MMC de certificados do Microsoft Windows (que permite que o assistente de solicitação de certificado seja invocado). Se outros protocolos de camada de transporte forem usados com os serviços de certificados, um desenvolvedor poderá criar um intermediário para cada protocolo de camada de transporte desejado.

Os intermediários se comunicam com os serviços de certificados usando as interfaces [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) fornecidas pelo mecanismo do servidor. O método [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) é usado para enviar uma [*solicitação de certificado*](../secgloss/c-gly.md)e [**ICertRequest:: getcertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) é usado para obter o certificado emitido resultante. Da mesma forma, [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) é usado para determinar qual autoridade de certificação pode ser usada para emitir o certificado.

Um intermediário não depende do idioma. Pode ser um programa escrito em C++, Visual Basic, Java, script ou outra linguagem.

Além de coletar dados do cliente para criar uma solicitação de certificado, um intermediário pode especificar atributos de solicitação. As solicitações enviadas a uma [*autoridade de certificação*](../secgloss/c-gly.md) que executa o módulo de política corporativa devem indicar o tipo de certificado solicitado especificando um atributo "certificatetemplate" ou uma extensão de modelo de certificado na própria solicitação.

Observe que durante a criação de uma solicitação de certificado, os desenvolvedores (e intermediários) são responsáveis por manter o sigilo da chave privada. Depois que uma chave privada foi comprometida (perdeu seu sigilo), ela é inútil.

As páginas de registro da Web dos serviços de certificados usam as [interfaces de registro de certificado](cryptography-interfaces.md), que protegem as chaves privadas gerando-as na estação de trabalho. Além de manter o sigilo da chave privada, o controle de registro de certificado permite que um intermediário especifique o provedor de serviços de criptografia, a especificação de chave, a restrição de chave e o algoritmo de hash.

O snap-in do MMC de certificados também usa o controle de registro de certificado (Xenroll.dll). No entanto, onde as páginas de registro da Web dos serviços de certificados fazem com que o recurso de controle de registro de certificado (Xenroll.dll) seja baixado para o cliente, se necessário, o snap-in do MMC de certificados é executado em um ambiente em que Xenroll.dll já é um recurso disponível.

Além de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig), os desenvolvedores de intermediários podem encontrar as [interfaces de registro de certificado](cryptography-interfaces.md) e o controle de [registro de cartão inteligente](certificate-enrollment-control.md) para ser útil.

 

 
