---
description: O carimbo de data/hora de Authenticode baseia-se nas \# contraassinaturas PKCS 9 padrão. As ferramentas de assinatura da Microsoft permitem que os desenvolvedores afixam carimbos de data/hora ao mesmo tempo que fixam as assinaturas Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Carimbo de data/hora das assinaturas Authenticode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3631d402da56d4078cecce65075c92dff0ec7e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169686"
---
# <a name="time-stamping-authenticode-signatures"></a>Carimbo de data/hora das assinaturas Authenticode

As assinaturas do Authenticode da Microsoft fornecem garantias de autorização e criação para dados binários. O carimbo de data/hora de Authenticode baseia-se nas \# contraassinaturas PKCS 9 padrão. As ferramentas de assinatura da Microsoft permitem que os desenvolvedores afixam carimbos de data/hora ao mesmo tempo que fixam as assinaturas Authenticode. O carimbo de data/hora permite que as assinaturas Authenticode sejam verificadas mesmo depois que os certificados usados para a assinatura expirarem.

## <a name="a-brief-introduction-to-authenticode"></a>Uma breve introdução ao Authenticode

O [*Authenticode*](../secgloss/a-gly.md) aplica a tecnologia de assinatura digital para garantir a autoria e a integridade de dados binários, como software instalável. Um navegador da Web do cliente ou outros componentes do sistema podem usar as assinaturas Authenticode para verificar a integridade dos dados quando o software é baixado ou instalado. As assinaturas Authenticode podem ser usadas com muitos formatos de software, incluindo. cab,. exe,. ocx e. dll.

A Microsoft mantém uma lista de CAS ( [*autoridades de certificação*](/security/trusted-root/participants-list) ) públicas. Os emissores de certificados Authenticode atualmente incluem [SSL.com](https://www.ssl.com/), [DigiCert](https://www.digicert.com/), [Sectigo (Comodo)](https://www.sectigo.com/)e [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Sobre o carimbo de data/hora criptográfico

No passado, uma variedade de métodos de carimbo de hora criptográfico foi proposta. Consulte, por exemplo, Haber e Stornetta "como Time-Stamp um documento digital" no *diário de Cryptology* (1991) e Benaloh e de Mare "acumuladores unidirecionais: uma alternativa descentralizada para assinaturas digitais" em notas de *palestra Springer-Verlag em Computer Science* Vol. 765 (EUROCRYPT ' 93). Um resumo estendido deste artigo está disponível no [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a). (Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.) Como o tempo é um físico, em vez de uma quantidade matemática, esses métodos geralmente se preocupam com como vincular objetos para que a ordem de criação possa ser determinada ou como agrupar objetos com eficiência que podem ser descritos como tendo sido criados simultaneamente.

Os sistemas que tentam autenticar o tempo como uma quantidade sempre exigem alguma forma de confiança. Em uma configuração fortemente antagônico, protocolos complexos podem ser usados para garantir algum grau de sincronia. No entanto, esses protocolos exigem uma ampla interação entre as partes afetadas. Na prática, se uma só precisar de certificação de tempo de uma fonte confiável, a origem poderá simplesmente agir como uma notary fornecendo uma instrução assinada (certificação) de que o objeto foi apresentado para assinatura no horário indicado.

O método de metaassinatura do carimbo de data/hora implementado abaixo permite que as assinaturas sejam verificadas mesmo após o certificado de autenticação ter expirado ou ter sido revogado. O carimbo de data/hora permite que o verificador saiba de forma confiável o tempo que a assinatura foi afixada e, portanto, confie na assinatura se ela era válida naquele momento. A hora Stamper deve ter uma fonte de tempo confiável e protegida.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>\#Documentos assinados PKCS 7 e referendas

\#O PKCS 7 é um formato padrão para dados criptográficos, incluindo dados assinados, certificados e [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs). O tipo PKCS \# 7 específico de interesse no contexto de carimbo de data/hora são dados assinados, correspondendo ao \# tipo de conteúdo [**SignedData**](signeddata.md) definido PKCS 7.

O \# pacote PKCS 7 consiste em [**SignedData**](signeddata.md) que identifica o conteúdo real e determinadas informações sobre ele e os blocos de assinatura SignerInfo. Um SignerInfo pode conter uma referenda, o que recursivamente é outro SignerInfo. Em princípio, uma sequência dessas referendas pode estar presente. A referenda é um atributo não autenticado em relação à assinatura no SignerInfo; ou seja, ele pode ser afixado subsequentemente à assinatura original. No formulário de estrutura de tópicos:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Versão (do PKCS \# 7, geralmente versão 1)
-   DigestAlgorithms (coleção de todos os algoritmos usados por SignerInfo blocos de assinatura para processamento otimizado)
-   ContentInfo (contentType é igual a [**SignedData**](signeddata.md), mais conteúdo ou referência a conteúdo)
-   Certificados OPCIONais (coleção de todos os certificados usados)
-   CRLs OPCIONais (coleção de todas as CRLs)
-   Blocos de assinatura SignerInfo (a assinatura real, composta de um ou mais blocos de assinatura SignerInfo)

SignerInfo (o bloco de assinatura)

-   Versão (do PKCS \# 7, geralmente versão 1)
-   Certificado (emissor e número de série para identificar exclusivamente o certificado do signatário em [**SignedData**](signeddata.md))
-   DigestAlgorithm mais o DigestEncryptionAlgorithm mais o resumo (hash), além do EncryptedDigest (assinatura real)
-   AuthenticatedAttributes opcional (por exemplo, assinado por este signatário)
-   UnauthenticatedAttributes opcional (por exemplo, não assinado por este signatário)

Um exemplo de um atributo autenticado é o tempo de assinatura (OID 1.2.840.113549.1.9.5) porque faz parte do que o serviço de carimbo de data/hora assina. Um exemplo de um atributo não autenticado é a referenda (OID 1.2.840.113549.1.9.6), pois ele pode ser fixado após a assinatura. Nesse caso, o próprio SignerInfo contém um SignerInfo (a referenda).

> [!Note]  
> O objeto que está assinado na referenda é a assinatura original (ou seja, o EncryptedDigest do SignerInfo original).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool e o processo de Authenticode

[SignTool](signtool.md) está disponível para assinatura Authenticode e dados binários de carimbo de data/hora. A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.

Os dados binários de assinatura e carimbo de data/hora são relativamente simples usando [SignTool](signtool.md). O Publicador deve obter um certificado de assinatura de código de uma AC de assinatura de código comercial. Para sua conveniência, a Microsoft publica e atualiza uma lista de CAs públicas, incluindo aquelas que emitem certificados Authenticode. Quando estiver pronto para publicar, os arquivos de objeto serão assinados e marcados com o tempo usando parâmetros de linha de comando apropriados com a ferramenta SignTool. O resultado de qualquer operação de SignTool é sempre um \# formato PKCS 7 [**SignedData**](signeddata.md).

O SignTool aceita como entrada dados binários brutos para serem assinados e marcados com carimbo de data/hora ou dados binários assinados anteriormente para serem carimbados. Os dados que foram assinados anteriormente podem ser carimbados com o uso do comando de **carimbo de data/** hora de SignTool.



| Argumento             | Descrição                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/T** *HTTPAddress* | Indica que o arquivo deve ser carimbado com o tempo. Uma URL que especifica um endereço de um servidor de carimbo de data/hora deve ser fornecida. **/t** pode ser usado com os comandos de **saída de SignTool** e de **carimbo de data/hora de SignTool** . |



 

Para obter mais informações sobre as ferramentas que podem ser úteis nesse contexto, consulte [ferramentas de criptografia](cryptography-tools.md) e [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Detalhes da implementação e formato de conexão

O [SignTool](signtool.md) conta com a implementação Authenticode do Windows para criar e assinaturas de carimbo de data/hora. O [*Authenticode*](../secgloss/a-gly.md) opera em arquivos binários, por exemplo,. cab,. exe,. dll ou. ocx. O Authenticode primeiro cria a assinatura, produzindo \# um [**SignedData**](signeddata.md)PKCS 7. É essa **SignedData** que deve ser assinada por você, conforme descrito no PKCS \# 9.

O processo de referendas ocorre em quatro etapas:

1.  Copie a assinatura (ou seja, a encryptedDigest) da SignerInfo do \# [**SignedData**](signeddata.md)PKCS 7.
2.  Construa uma solicitação de carimbo de data/hora cujo conteúdo é a assinatura original. Envie-o para a [*notação de sintaxe abstrata*](../secgloss/a-gly.md) do servidor de carimbo de data/hora (ASN. 1) codificada como um TimeStampRequest.
3.  Receba um carimbo de data/hora, formatado como um segundo \# [**SignedData**](signeddata.md)PKCS 7, retornado do servidor de carimbo de data/hora.
4.  Copie o SignerInfo do carimbo de data/hora diretamente para o \# [**SignedData**](signeddata.md)PKCS 7 original, como uma \# metaassinatura PKCS 9 (ou seja, um atributo não autenticado no SignerInfo do original).

## <a name="time-stamp-request"></a>Solicitação de carimbo de data/hora

A solicitação de carimbo de data/hora é enviada em uma mensagem de POSTAgem HTTP 1,1. No cabeçalho HTTP, a diretiva CacheControl é definida como no-cache e a diretiva Content-Type é definida como application/octet-stream. O corpo da mensagem HTTP é uma codificação Base64 de codificação [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) da solicitação de carimbo de data/hora.

Embora não esteja sendo usado no momento, a diretiva Content-Length também deve ser usada na construção da mensagem HTTP, pois ajuda o servidor de carimbo de data/hora localizar onde a solicitação está dentro do HTTP POST.

Outros cabeçalhos HTTP também podem estar presentes e devem ser ignorados se não forem compreendidos pelo solicitante ou pelo servidor de carimbo de data/hora.

A solicitação de carimbo de data/hora é uma mensagem codificada pelo ASN. 1. O formato da solicitação é o seguinte.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

O referenda é o identificador de [*objeto*](../secgloss/o-gly.md) (OID) que identifica isso como uma referenda de carimbo de data/hora e deve ser o OID 1.3.6.1.4.1.311.3.2.1 exato.

Nenhum atributo está incluído atualmente na solicitação de carimbo de data/hora.

O conteúdo é um ContentInfo, conforme definido pelo PKCS \# 7. O conteúdo são os dados a serem assinados. Para o carimbo de data/hora de assinatura, o ContentType deve ser dado, e o conteúdo deve ser o encryptedDigest (assinatura) do SignerInfo do \# conteúdo PKCS 7 a ser carimbado.

## <a name="time-stamp-response"></a>Resposta de carimbo de data/hora

A resposta de carimbo de data/hora também é enviada em uma mensagem HTTP 1,1. No cabeçalho HTTP, a diretiva Content-Type também é definida como application/octet-stream. O corpo da mensagem HTTP é uma codificação Base64 da codificação DER da resposta de carimbo de data/hora.

A resposta de carimbo de data/hora é uma \# mensagem assinada PKCS 7 assinada pela hora Stamper. O ContentInfo da mensagem PKCS \# 7 é idêntico ao ContentInfo recebido no carimbo de data/hora. O \# conteúdo PKCS 7 contém o atributo autenticado de tempo de assinatura (definido em PKCS \# 99, OID 1.2.840.113549.9.5).

Depois que o Authenticode recebe o carimbo de data/hora do servidor, o Authenticode incorpora o carimbo de data/hora ao \# [**SignedData**](signeddata.md) PKCS 7 original como uma referenda. Para fazer isso, o ContentInfo do \# **SignedData** PKCS 7 retornado é Descartado e o SignerInfo do carimbo de data/hora retornado é copiado como uma referenda no SIGNERINFO do \# **SignedData** PKCS 7 original. A cadeia de certificados da hora Stamper também é copiada em certificados no SignedData PKCS \# 7  original como um atributo não autenticado do assinante original.

Para obter mais informações sobre PKCS e outros assuntos de segurança, consulte a [biblioteca de conteúdo do site da RSA](https://www.rsa.com/content_library.aspx).

 

 
