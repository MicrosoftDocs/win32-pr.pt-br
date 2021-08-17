---
description: Os Serviços de Certificados são compatíveis com o uso de certificados conforme definido na recomendação de ITU-T X.509 (além disso, ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propriedades do Certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48850b812c8a8227f41229ccbaa88259805d61a199d695f4a90d4652a94b99dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771561"
---
# <a name="certificate-properties"></a>Propriedades do Certificado

Os Serviços de Certificados são compatíveis com o uso de certificados conforme definido na recomendação de ITU-T [*X.509*](../secgloss/x-gly.md) (além disso, ISO/IEC 9594-8). A seguir estão as propriedades contidas em um certificado X.509 padrão.



| Campo                                       | Descrição                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão                                     | Número de versão do formato do certificado.                                                                                                                                                                       |
| Número de Série                               | Número de série do certificado. Esse número é atribuído pelo emissor e é exclusivo na lista de certificados emitidos pelo emissor.                                                                          |
| Parâmetros e identificador de algoritmo         | Algoritmo de assinatura e todos os parâmetros usados pelo emissor.                                                                                                                                                      |
| Emissor                                      | Nome da autoridade [*de certificação*](../secgloss/c-gly.md) que emitiu o certificado.                                               |
| Não antes (Data)                           | O certificado não é válido antes dessa data.                                                                                                                                                                         |
| Não após (Data)                            | O certificado não é válido após essa data.                                                                                                                                                                          |
| Nome do assunto                                | Nome da pessoa ou entidade para a qual o certificado está sendo emitido. Esse campo também pode incluir a organização do destinatário do certificado, a unidade da organização, a localidade, o estado ou a província e o país/região. |
| Parâmetros e algoritmos de chave pública da assunto | O algoritmo e os parâmetros usados para a chave pública [*do assunto.*](../secgloss/p-gly.md)                                                                       |
| Chave pública do assunto                          | A chave pública real (uma cadeia de caracteres de bits).                                                                                                                                                                           |
| Assinatura                                   | Assinatura conforme fornecido pelo emissor.                                                                                                                                                                            |



 

Um certificado pode conter os itens a seguir, dependendo da [*versão X.509*](../secgloss/x-gly.md) do certificado.



| Campo opcional    | Descrição                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID Exclusiva do Emissor  | Usado para tornar o nome do emissor não ambíguo se ele tiver sido usado por mais de uma entidade. Presente somente nas versões [*X.509*](../secgloss/x-gly.md) 2.0 ou posterior.<br/> |
| ID exclusiva do assunto | Usado para tornar o nome da entidade não ambíguo se ele tiver sido usado por mais de uma entidade. Presente somente no X.509 2.0 ou posterior.<br/>                                                                     |
| Extensões        | Para especificar as propriedades personalizadas desejadas. Qualquer número de campos de extensão pode ser incluído no certificado. Presente somente na versão X.509 3.0.<br/>                                            |



 

> [!Note]  
> Os Serviços de Certificados da Microsoft emitem certificados X.509 versão 3.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de nome](name-properties.md)
</dt> </dl>

 

 
