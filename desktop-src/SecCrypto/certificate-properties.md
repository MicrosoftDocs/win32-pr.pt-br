---
description: Os serviços de certificados dão suporte ao uso de certificados, conforme definido na recomendação ITU-T X. 509 (também, ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propriedades do Certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828011"
---
# <a name="certificate-properties"></a>Propriedades do Certificado

Os serviços de certificados dão suporte ao uso de certificados, conforme definido na recomendação ITU-T [*X. 509*](../secgloss/x-gly.md) (também, ISO/IEC 9594-8). Veja a seguir as propriedades contidas em um certificado X. 509 padrão.



| Campo                                       | Descrição                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão                                     | Número de versão do formato do certificado.                                                                                                                                                                       |
| Número de Série                               | Número de série do certificado. Esse número é atribuído pelo emissor e é exclusivo na lista de certificados emitidos do emissor.                                                                          |
| Identificador e parâmetros do algoritmo         | Algoritmo de assinatura e quaisquer parâmetros usados pelo emissor.                                                                                                                                                      |
| Emissor                                      | Nome da [*autoridade de certificação*](../secgloss/c-gly.md) que emitiu o certificado.                                               |
| Não antes (Data)                           | O certificado não é válido antes desta data.                                                                                                                                                                         |
| Não após (Data)                            | Certificado inválido após esta data.                                                                                                                                                                          |
| Nome do assunto                                | Nome da pessoa ou entidade para a qual o certificado está sendo emitido. Esse campo também pode incluir a organização do destinatário do certificado, a unidade organizacional, a localidade, o estado ou a província e o país/região. |
| Algoritmo e parâmetros de chave pública da entidade | O algoritmo e os parâmetros usados para a [*chave pública*](../secgloss/p-gly.md)da entidade.                                                                       |
| Chave pública de assunto                          | A chave pública real (uma cadeia de caracteres de bits).                                                                                                                                                                           |
| Assinatura                                   | Assinatura conforme fornecida pelo emissor.                                                                                                                                                                            |



 

Um certificado pode conter os seguintes itens, dependendo da versão [*X. 509*](../secgloss/x-gly.md) do certificado.



| Campo opcional    | Descrição                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID exclusiva do emissor  | Usado para tornar o nome do emissor inambíguo se ele tiver sido usado por mais de uma entidade. Presente somente nas versões [*X. 509*](../secgloss/x-gly.md) 2,0 ou posterior.<br/> |
| ID exclusiva da entidade | Usado para tornar o nome da entidade inequívoca se ele tiver sido usado por mais de uma entidade. Presente somente em X. 509 2,0 ou posterior.<br/>                                                                     |
| Extensões        | Para especificar as propriedades personalizadas desejadas. Qualquer número de campos de extensão pode ser incluído no certificado. Presente somente na versão X. 509 3,0.<br/>                                            |



 

> [!Note]  
> O Microsoft Certificate Services emite certificados X. 509 versão 3.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do nome](name-properties.md)
</dt> </dl>

 

 
