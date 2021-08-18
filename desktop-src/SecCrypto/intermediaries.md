---
description: Intermediários se comunicam com aplicativos cliente para permitir que eles enviem solicitações de certificado e (supondo que a solicitação resulta em um certificado emitido) para baixar o certificado emitido para o cliente.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: intermediários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f9dbd48d5af575658c04760740ad0b1f64f373d76bb20ba80253b874c67de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005284"
---
# <a name="intermediaries"></a>intermediários

Intermediários se comunicam com aplicativos [](../secgloss/c-gly.md)cliente para permitir que eles enviem solicitações de certificado e (supondo que a solicitação resulta em um certificado emitido) para baixar o certificado emitido para o cliente. Cada protocolo de camada de transporte requer seu próprio intermediário.

Os Serviços de Certificados da Microsoft são fornecidas com um intermediário (as páginas de registro da Web) para HTTP. Outro exemplo de um intermediário é o snap-in MMC Windows Microsoft Windows (que permite que o Assistente de Solicitação de Certificado seja invocado). Se outros protocolos de camada de transporte devem ser usados com os Serviços de Certificados, um desenvolvedor pode criar um intermediário para cada protocolo de camada de transporte desejado.

Os intermediários se comunicam com os Serviços de Certificados usando as interfaces [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) fornecidas pelo mecanismo de servidor. O [**método ICertRequest::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) é [](../secgloss/c-gly.md)usado para enviar uma solicitação de certificado e [**ICertRequest::GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) é usado para obter o certificado emitido resultante. Da mesma forma, [**ICertConfig::GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) é usado para determinar qual autoridade de certificação pode ser usada para emitir o certificado.

Um intermediário não depende do idioma. Pode ser um programa escrito em C++, Visual Basic, Java, script ou outra linguagem.

Além de coletar dados do cliente para criar uma solicitação de certificado, um intermediário pode especificar atributos de solicitação. As solicitações enviadas [*a*](../secgloss/c-gly.md) uma autoridade de certificação que executa o módulo de política corporativa devem indicar o tipo de certificado solicitado especificando um atributo "CertificateTemplate" ou uma extensão de Modelo de Certificado na própria solicitação.

Observe que, durante a criação de uma solicitação de certificado, os desenvolvedores (e intermediários) são responsáveis por manter o segredo da chave privada. Depois que uma chave privada for comprometida (perder seu segredo), ela será inútil.

As páginas de registro na Web dos Serviços de Certificados usam as [Interfaces](cryptography-interfaces.md)de Registro de Certificado, que protegem as chaves privadas gerando-as na estação de trabalho. Além de manter o segredo da chave privada, o Controle de Registro de Certificado permite que um intermediário especifique o provedor de serviços criptográfico, a especificação da chave, a força da chave e o algoritmo de hash.

O snap-in do MMC de Certificados também usa o controle de registro de certificado (Xenroll.dll). No entanto, quando as páginas de registro na Web dos Serviços de Certificados faz com que o recurso de Controle de Registro de Certificado (Xenroll.dll) seja baixado para o cliente, se necessário, o snap-in do MMC de Certificados é executado em um ambiente em que Xenroll.dll já é um recurso disponível.

Além de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig,**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)os desenvolvedores de [intermediários](cryptography-interfaces.md) [](certificate-enrollment-control.md) podem achar as Interfaces de Registro de Certificado e o Controle de Registro de Cartão Inteligente úteis.

 

 
