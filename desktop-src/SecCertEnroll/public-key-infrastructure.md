---
description: A criptografia de chave pública (também chamada de criptografia de chave assimétrica) usa um par de chaves para criptografar e descriptografar conteúdo.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infraestrutura de chave pública
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e4ff0b2b3912bc44851be105c2e2b15200eb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755960"
---
# <a name="public-key-infrastructure"></a>Infraestrutura de chave pública

A criptografia de chave pública (também chamada de criptografia de chave assimétrica) usa um par de chaves para criptografar e descriptografar conteúdo. O par de chaves consiste em uma chave pública e uma privada que estão matematicamente relacionadas. Um indivíduo que pretende se comunicar com segurança com outras pessoas pode distribuir a [*chave pública*](/windows/desktop/SecGloss/p-gly) , mas deve manter o segredo da [*chave privada*](/windows/desktop/SecGloss/p-gly) . O conteúdo criptografado usando uma das chaves pode ser descriptografado usando o outro. Suponha, por exemplo, que Bob deseja enviar uma mensagem de email segura para Alice. Isso pode ser feito da seguinte maneira:

1.  Bob e Alice têm seus próprios pares de chaves. Eles mantiveram suas chaves privadas com segurança e enviaram suas chaves públicas diretamente entre si.
2.  Bob usa a chave pública de Alice para criptografar a mensagem e a envia para ela.
3.  Alice usa sua chave privada para descriptografar a mensagem.

Este exemplo simplificado destaca pelo menos uma preocupação óbvia que Bob deve ter sobre a chave pública que ele usou para criptografar a mensagem. Ou seja, ele não pode saber com certeza que a chave que ele usou para criptografia realmente pertencia a Alice. É possível que outra parte que esteja monitorando o canal de comunicação entre Bob e Alice substitua uma chave diferente.

O conceito de infraestrutura de chave pública evoluiu para ajudar a resolver esse problema e outros. Uma PKI (infraestrutura de chave pública) consiste em elementos de software e hardware que um terceiro confiável pode usar para estabelecer a integridade e a propriedade de uma chave pública. A parte confiável, chamada de [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA), normalmente faz isso emitindo certificados binários assinados (criptografados) que afirmam a identidade da entidade do certificado e associam essa identidade à chave pública contida no certificado. A CA assina o certificado usando sua chave privada. Ele emite a chave pública correspondente a todas as partes interessadas em um certificado de autoridade de certificação autoassinado. Quando uma AC é usada, o exemplo anterior pode ser modificado da seguinte maneira:

1.  Suponha que a autoridade de certificação emitiu um certificado digital assinado que contém sua chave pública. A AC assina automaticamente esse certificado usando a chave privada que corresponde à chave pública no certificado.
2.  Alice e Bob concordam em usar a AC para verificar suas identidades.
3.  Alice solicita um certificado de chave pública da AC.
4.  A autoridade de certificação verifica sua identidade, computa um hash do conteúdo que criará seu certificado, assina o hash usando a chave privada que corresponde à chave pública no certificado de autoridade de certificação publicado, cria um novo certificado concatenando o conteúdo do certificado e o hash assinado e disponibiliza o novo certificado publicamente.
5.  Bob recupera o certificado, descriptografa o hash assinado usando a chave pública da autoridade de certificação, computa um novo hash do conteúdo do certificado e compara os dois hashes. Se os hashes corresponderem, a assinatura será verificada e Bob poderá pressupor que a chave pública no certificado realmente pertence a Alice.
6.  Bob usa a chave pública verificada de Alice para criptografar uma mensagem para ela.
7.  Alice usa sua chave privada para descriptografar a mensagem de Bob.

Em resumo, o processo de assinatura de certificado permite que Bob Verifique se a chave pública não foi violada ou corrompida durante o trânsito. Antes de emitir um certificado, a autoridade de certificação armazena em hash o conteúdo, assina (criptografa) o hash usando sua própria chave privada e inclui o hash criptografado no certificado emitido. Bob verifica o conteúdo do certificado descriptografando o hash com a chave pública da CA, executando um hash separado do conteúdo do certificado e comparando os dois hashes. Se eles corresponderem, Bob poderá ser razoavelmente certo de que o certificado e a chave pública que ele contém não foram alterados.

Uma PKI típica consiste nos seguintes elementos.

| Elemento                            | Descrição                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Autoridade de certificação<br/> | Atua como a raiz de confiança em uma infraestrutura de chave pública e fornece serviços que autenticam a identidade de indivíduos, computadores e outras entidades em uma rede.<br/>      |
| Autoridade de registro<br/>  | É certificado por uma autoridade de certificação raiz para emitir certificados para usos específicos permitidos pela raiz. Em uma PKI da Microsoft, uma RA (autoridade de registro) é geralmente chamada de autoridade de certificação subordinada.<br/> |
| Banco de dados de certificados<br/>    | Salva solicitações de certificado e certificados emitidos e revogados e solicitações de certificado na CA ou RA.<br/>                                                                       |
| Repositório de certificados<br/>       | Salva os certificados emitidos e solicitações de certificado pendentes ou rejeitadas no computador local.<br/>                                                                                  |
| Servidor de arquivamento de chave<br/>     | Salva as chaves privadas criptografadas no banco de dados de certificado para recuperação após a perda.<br/>                                                                                              |



 

A API de registro de certificado permite que você envie solicitações de arquivamento de certificado e chave para autoridades de certificação e de registro e instale o certificado emitido em um computador local. Ele não permite que você manipule diretamente o repositório de certificados ou o banco de dados de certificado.

Os tópicos a seguir abordam a infraestrutura de chave pública da Microsoft com mais detalhes:

-   [Certificados de chave pública X. 509](about-x-509-public-key-certificates.md)
-   [Elementos PKI](about-pki-components.md)
-   [Modelos de confiança](about-trust-models.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API de registro de certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

