---
description: Os aplicativos que assinam e verificam assinaturas digitais XML devem ser escritos de acordo com as práticas recomendadas a seguir para evitar ataques de negação de serviço, perda de dados e comprometimento de informações privadas.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Considerações de segurança de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e54b4c5f3f863e0bc84172a7507bfe8609e2df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779938"
---
# <a name="xml-digital-signature-security-considerations"></a>Considerações de segurança de assinatura digital XML

Os aplicativos que assinam e verificam assinaturas digitais XML devem ser escritos de acordo com as práticas recomendadas a seguir para evitar ataques de negação de serviço, perda de dados e comprometimento de informações privadas. A lista a seguir fornece diretrizes gerais; no entanto, os desenvolvedores são incentivados a executar análise de segurança adicional específica para seus aplicativos e examinar as práticas recomendadas mais recentes das assinaturas digitais publicadas pelo W3C.

-   [Verificar a confiança da chave de assinatura](#verify-trust-of-the-signing-key)
-   [Primeiro, verifique a chave de assinatura e valide SignedInfo e, em seguida, valide as referências](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Use o conjunto mínimo de algoritmos de canonização e transformações necessárias](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Garantir que os URIs de destino apontem para destinos dentro do escopo esperado](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Verifique se os dados consumidos pelo aplicativo são verificados pela assinatura](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Siga as melhores práticas de criptografia](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Verificar a confiança da chave de assinatura

Verifique se a chave de assinatura é confiável verificando o certificado [*X. 509*](../secgloss/x-gly.md) correspondente (e a cadeia de certificados) incluídos na mensagem assinada. Como alternativa, a confiança na chave de assinatura pode ser estabelecida em um modo fora de banda, como um administrador Configurando um conjunto de chaves confiáveis ou um aplicativo consultando um serviço confiável em um canal seguro.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Primeiro, verifique a chave de assinatura e valide SignedInfo e, em seguida, valide as referências

Verifique a relação de confiança na chave de assinatura e a integridade do elemento **SignedInfo** antes de validar as referências. Da mesma forma, os aplicativos devem validar os elementos do **manifesto** antes de resolver as referências contidas nos elementos do **manifesto** . Elementos de **referência** permitem a especificação de URIs de destino, transformações e algoritmos de canonização. Se não for validado, esses campos poderão potencialmente ser usados para criar negação de serviço, perda de dados ou outros ataques.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Use o conjunto mínimo de algoritmos de canonização e transformações necessárias

XSLT e XPATH não devem ser usados em elementos não autenticados, como **KeyInfo**. Se um aplicativo exigir o uso de XPath, restrinja o conjunto de expressões XPATH permitidas apenas aos que usam os eixos ancestral ou self e não Calcule o valor da cadeia de caracteres de elementos. Por padrão, o CryptXML dá suporte a um conjunto limitado de algoritmos de canonização (consulte URIs com suporte em [algoritmos criptográficos de assinatura digital XML](xml-digital-signature-cryptographic-algorithms.md)). Os desenvolvedores podem implementar transformações adicionais ou algoritmos de canonização para uso em seu aplicativo. No entanto, o uso de algoritmos complexos cria a possibilidade de ataques de negação de serviço ou de interrupção das características de repúdio de uma assinatura. Nos casos em que as transformações são exigidas pelo aplicativo, limite o número de transformações que podem ser especificadas por referência ao número mais alto exigido pelo aplicativo. Essa prática reduz ataques de negação de serviço com base no uso excessivo de transformações.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Garantir que os URIs de destino apontem para destinos dentro do escopo esperado

Os aplicativos devem limitar os URIs de destino para o menor escopo exigido pelo aplicativo. Por exemplo, pode ser esperado que os URIs apontem para destinos no mesmo documento, arquivos em um diretório de destino específico ou locais de rede dentro de um domínio DNS específico. Os URIs definidos por um invasor para apontar para fora do domínio esperado podem fazer com que um aplicativo recupere conteúdo mal-intencionado, envie solicitações HTTP mal-intencionadas (possivelmente contendo cadeias de caracteres de consulta) ou faça com que os aplicativos se autentiquem em servidores mal-intencionados.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Verifique se os dados consumidos pelo aplicativo são verificados pela assinatura

Se o aplicativo validar a chave de assinatura e os elementos **SignedInfo** e **Reference** , mas o aplicativo consumir dados importantes não referenciados pela assinatura, a assinatura não fornecerá nenhuma proteção significativa. O significado semântico de uma assinatura pode variar com base na posição da assinatura dentro do documento. Os aplicativos são incentivados a verificar a posição da assinatura em um documento. Além disso, verifique a posição dos dados referenciados e os nomes de elementos para atenuar os ataques de substituição e encapsulamento.

## <a name="follow-best-cryptographic-practices"></a>Siga as melhores práticas de criptografia

Os algoritmos criptográficos se tornam mais fracos ao longo do tempo à medida que novos ataques são descobertos e mais energia de computação fica disponível. Não codifique os identificadores de algoritmos criptográficos ou os tamanhos de chave em seus aplicativos. Para obter uma lista mais completa das melhores práticas de criptografia, consulte Michael Howard e Steve Lipner, "padrões de criptografia mínimas do SDL", no *ciclo de vida do desenvolvimento da segurança* (Redmond, Washington: Microsoft Press, 2006), 251 – 258.

As práticas recomendadas adicionais podem ser encontradas no site do W3C: https://www.w3.org .

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.

 

 

 
