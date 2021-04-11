---
description: Um certificado X.509 versão 3 contém os campos definidos na versão 1 e 2, e adiciona extensões de certificado. A sintaxe ASN. 1 das extensões de certificado é mostrada no exemplo a seguir.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensões da versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169487"
---
# <a name="version-3-extensions"></a>Extensões da versão 3

Um certificado X.509 versão 3 contém os campos definidos na versão 1 e 2, e adiciona extensões de certificado. A sintaxe ASN. 1 das extensões de certificado é mostrada no exemplo a seguir.

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

As extensões padrão da versão 3 e seus identificadores de objeto (OIDs) são listados na tabela a seguir. A Microsoft oferece suporte a eles e inclui extensões personalizadas adicionais. Para obter mais informações, consulte [extensões](extensions.md).

| Extensão                                         | Descrição                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de chave de autoridade (2.5.29.19)<br/>    | Identifica a chave pública da autoridade de certificação (AC) que corresponde à chave privada da AC usada para assinar o certificado.                                                                              |
| Restrições básicas (2.5.29.35)<br/>           | Especifica se a entidade pode ser usada como AC e, em caso afirmativo, o número de ACs subordinadas que podem existir abaixo dela na cadeia de certificados.                                                           |
| Políticas de certificado (2.5.29.32)<br/>        | Especifica as políticas sob as quais o certificado foi emitido e as finalidades para as quais ele pode ser usado.                                                                                            |
| Pontos de distribuição de CRL (2.5.29.31)<br/>     | Contém o URI da CRL ( [*lista de certificados revogados*](/windows/desktop/SecGloss/c-gly) ) base.                                  |
| Uso avançado de chave (2.5.29.46)<br/>          | Especifica a maneira na qual a chave pública contida no certificado pode ser usada.                                                                                                                   |
| Nome alternativo do emissor (2.5.29.8)<br/>      | Especifica uma ou mais formas de nome alternativas para o emissor da solicitação de certificado.                                                                                                                  |
| Uso de chave (2.5.29.15)<br/>                   | Especifica restrições nas operações que podem ser executadas pela chave pública contida no certificado.                                                                                           |
| Restrições de nome (2.5.29.30)<br/>            | Especifica o namespace dentro do qual todos os nomes de entidades em uma hierarquia de certificados devem estar localizados. A extensão é usada somente em um certificado de AC.                                                       |
| Restrições de política (2.5.29.36)<br/>          | Restringe a validação do caminho, proibindo o mapeamento de política ou exigindo que cada certificado na hierarquia contenha um identificador de política aceitável. A extensão é usada somente em um certificado de AC. |
| Mapeamentos de política (2.5.29.33)<br/>             | Especifica as políticas em uma AC subordinada que correspondem às políticas na AC emissora.                                                                                                                |
| Período de uso de chave privada (2.5.29.16)<br/>    | Especifica um período de validade para a chave privada diferente do período para o certificado com o qual a chave privada está associada.                                                                             |
| Nome alternativo da entidade (2.5.29.17)<br/>    | Especifica uma ou mais formas de nome alternativas para a entidade da solicitação de certificado. Dentre os exemplos de formas alternativas incluem-se endereços de email, nomes DNS, endereços IP e URIs.                           |
| Atributos de diretório de assunto (2.5.29.9)<br/> | Expressa atributos de identificação, como a nacionalidade da entidade do certificado. O valor da extensão é uma sequência de pares de valores OID.                                                              |
| Identificador de chave de entidade (2.5.29.14)<br/>      | Diferencia entre várias chaves públicas mantidas pela entidade do certificado. O valor da extensão é geralmente um hash SHA-1 da chave.                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Campos básicos](about-basic-fields.md)
</dt> <dt>

[Campos da versão 2](about-version-2-fields.md)
</dt> <dt>

[Certificados de chave pública X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

