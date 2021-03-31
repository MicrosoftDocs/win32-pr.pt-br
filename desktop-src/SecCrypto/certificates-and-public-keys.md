---
description: Os serviços de certificados são uma base para a PKI (infraestrutura de chave pública) que fornece os meios para proteger e autenticar informações.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificados e chaves públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e01993673fe16c8401368ffaa7e8815c450dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827499"
---
# <a name="certificates-and-public-keys"></a>Certificados e chaves públicas

Os serviços de certificados são uma base para a PKI (infraestrutura de chave pública) que fornece os meios para proteger e autenticar informações. A relação entre um detentor do certificado, a identidade do titular do certificado e a [*chave pública*](../secgloss/p-gly.md) do detentor do certificado é uma parte crítica da PKI. Essa infraestrutura é composta pelas seguintes partes:

-   [O par de chaves pública/privada](#the-publicprivate-key-pair)
-   [A solicitação de certificado](#the-certificate-request)
-   [A autoridade de certificação](#the-certification-authority)
-   [O certificado](#the-certificate-request)
-   [A lista de certificados revogados](#the-certificate-revocation-list)
-   [Sua chave pública usada para criptografia](#your-public-key-used-for-encryption)
-   [Sua chave pública usada para verificação de assinatura](#your-public-key-used-for-signature-verification)
-   [Função de serviços de certificados da Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>O par de chaves pública/privada

A PKI requer o uso de [*pares de chaves pública/privada*](../secgloss/p-gly.md). A matemática de pares de chaves públicas/privadas está além do escopo desta documentação, mas é importante observar a relação funcional entre uma chave pública e uma privada. Os [*algoritmos criptográficos*](../secgloss/c-gly.md) PKI usam a [*chave pública*](../secgloss/p-gly.md) do receptor de uma mensagem criptografada para criptografar dados e a [*chave privada*](../secgloss/p-gly.md) relacionada e apenas a chave privada relacionada para descriptografar a mensagem criptografada.

Da mesma forma, uma [*assinatura digital*](../secgloss/d-gly.md) do conteúdo, descrita mais detalhadamente abaixo, é criada com a chave privada do signatário. A chave pública correspondente, que está disponível para todos, é usada para verificar essa assinatura. O sigilo da chave privada deve ser mantido porque a estrutura está separada depois que a chave privada é comprometida.

Dado tempo e recursos suficientes, um par de chaves pública/privada pode ser comprometido, ou seja, a chave privada pode ser descoberta. Quanto mais longa for a chave, mais difícil será usar a força bruta para descobrir a chave privada. Na prática, chaves suficientemente fortes podem ser usadas para tornar impossível determinar a chave privada em tempo hábil, tornando a infra-estrutura de chave pública um mecanismo de segurança viável.

Uma chave privada pode ser armazenada, em formato protegido, em um disco; nesse caso, ela só pode ser usada com esse computador específico, a menos que seja fisicamente movida para outro computador. Uma alternativa é ter uma chave em um cartão inteligente que possa ser usada em um computador diferente, desde que ele tenha um leitor de cartão inteligente e software de suporte.

A chave pública, mas não a chave privada, do assunto de um certificado digital é incluída como parte da solicitação de [*certificado*](../secgloss/c-gly.md). (Portanto, um par de chaves pública/privada deve existir antes de fazer a solicitação de certificado.) Essa chave pública se torna parte do certificado emitido.

## <a name="the-certificate-request"></a>A solicitação de certificado

Antes de um certificado ser emitido, uma [*solicitação de certificado*](../secgloss/c-gly.md) deve ser gerada. Essa solicitação se aplica a uma entidade, por exemplo, um usuário final, um computador ou um aplicativo. Para discussão, assuma que a entidade é você mesmo. Os detalhes da sua identidade estão incluídos na solicitação de certificado. Depois que a solicitação é gerada, ela é enviada para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA). Em seguida, a AC usa suas informações de identidade para determinar se a solicitação atende aos critérios da autoridade de certificação para emitir um certificado. Se a autoridade de certificação aprovar a solicitação, ela emitirá um certificado para você, como a entidade chamada na solicitação.

## <a name="the-certification-authority"></a>A autoridade de certificação

Antes de emitir seu certificado, a autoridade de certificação verifica sua identidade. Quando o certificado é emitido, sua identidade é associada ao certificado, que contém sua chave pública. Seu certificado também contém a assinatura digital da autoridade de certificação (que pode ser verificada por qualquer pessoa que receba seu certificado).

Como seu certificado contém a identidade da AC emissora, uma parte interessada que confia nessa autoridade de certificação pode estender essa relação de confiança ao seu certificado. A emissão de um certificado não estabelece confiança, mas transfere a confiança. Se o consumidor do certificado não confiar na AC emissora, ele não (ou pelo menos não deve) confiar em seu certificado.

Uma cadeia de certificados assinados permite que a confiança seja transferida para outras CAs também. Isso permite que as partes que usam diferentes CAs ainda possam confiar em certificados (desde que haja uma CA comum na cadeia, ou seja, uma AC que seja confiável para ambas as partes).

## <a name="the-certificate"></a>O certificado

Além da sua chave pública e da identidade da AC emissora, o certificado emitido contém informações sobre as finalidades de sua chave e certificado. Além disso, ele inclui o caminho para a lista de certificados revogados da autoridade de certificação e especifica o período de validade do certificado (datas de início e término).

Supondo que o consumidor do certificado confie na AC emissora do seu certificado, o consumidor do certificado deve determinar se o certificado ainda é válido, comparando as datas de início e término do certificado com a hora atual e verificando se o certificado não está na lista de certificados revogados da autoridade de certificação.

## <a name="the-certificate-revocation-list"></a>A lista de certificados revogados

Supondo que o certificado esteja sendo usado em um período de tempo válido e o consumidor de certificado confie na AC emissora, há mais um item para o consumidor de certificado verificar antes de usar o certificado: a CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ). O consumidor de certificado verifica a CRL da autoridade de certificação (o caminho para o qual está incluído como uma extensão no seu certificado) para garantir que o certificado não esteja na lista de certificados revogados. As CRLs existem porque há ocasiões em que um certificado não expirou, mas ele não pode mais ser confiável. Periodicamente, a AC publicará uma CRL atualizada. Os consumidores de certificado são responsáveis por comparar certificados com a CRL atual antes de considerar o certificado confiável.

## <a name="your-public-key-used-for-encryption"></a>Sua chave pública usada para criptografia

Se um remetente quiser criptografar uma mensagem antes de enviá-la para você, o remetente primeiro recuperará seu certificado. Depois que o remetente determina que a autoridade de certificação é confiável e seu certificado é válido e não revogado, o remetente usa sua chave pública (Lembre-se de que ele faz parte do certificado) com algoritmos criptográficos para criptografar a mensagem de [*texto*](../secgloss/p-gly.md) não criptografado em [*texto cifrado*](../secgloss/c-gly.md). Quando você receber o texto cifrado, use sua chave privada para descriptografar o texto cifrado.

Se um terceiro interceptar a mensagem de email de texto cifrado, o terceiro não poderá descriptografá-lo sem acesso à sua [*chave privada*](../secgloss/p-gly.md).

Observe que a massa das atividades listadas aqui é tratada pelo software, não diretamente pelo usuário.

## <a name="your-public-key-used-for-signature-verification"></a>Sua chave pública usada para verificação de assinatura

Uma [*assinatura digital*](../secgloss/d-gly.md) é usada como confirmação de que uma mensagem não foi alterada e como confirmação da identidade do remetente da mensagem. Essa assinatura digital depende de sua chave privada e do conteúdo da mensagem. Usando a mensagem como entrada e sua chave privada, os algoritmos criptográficos criam a assinatura digital. O conteúdo da mensagem não é alterado pelo processo de assinatura. Um destinatário pode usar sua chave pública (depois de verificar a validade do certificado, emitir a AC e o status de revogação) para determinar se a assinatura corresponde ao conteúdo da mensagem e determinar se a mensagem foi enviada por você.

Se um terceiro interceptar a mensagem pretendida, alterá-la (mesmo ligeiramente) e a encaminhará e a assinatura original para o destinatário, o destinatário, após o exame da mensagem e da assinatura, poderá determinar que a mensagem é suspeita. Da mesma forma, se um terceiro criar uma mensagem e enviá-la com uma assinatura digital falsa sob o forma que originou de você, o destinatário poderá usar sua chave pública para determinar que a mensagem e a assinatura não correspondam umas às outras.

O não- [*repúdio*](../secgloss/n-gly.md) também é suportado por assinaturas digitais. Se o remetente de uma mensagem assinada negar o envio da mensagem, o destinatário poderá usar a assinatura para refutar essa declaração.

Observe que a massa das atividades listadas aqui também é tratada pelo software, não diretamente pelo usuário.

## <a name="microsoft-certificate-services-role"></a>Função de serviços de certificados da Microsoft

Os serviços de certificados da Microsoft têm a função de emitir certificados ou negar solicitações de certificados, conforme orientado pelos módulos de política, que são responsáveis por garantir a identidade do solicitante de certificado. Os serviços de certificados também fornecem a capacidade de revogar um certificado, bem como publicar a CRL. Os serviços de certificados também podem ser distribuídos centralmente (por exemplo, para um serviço de diretório) certificados emitidos. A capacidade de emitir, distribuir, revogar e gerenciar certificados, juntamente com a publicação de CRLs, fornece os recursos necessários para a infraestrutura de chave pública.

 

 
