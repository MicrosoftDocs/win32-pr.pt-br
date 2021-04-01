---
description: Lista os valores de retorno de confiança do certificado e do certificado. Esses valores estão contidos no arquivo de cabeçalho Winerror. h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valores de retorno de certificado e de confiança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e17f170c7c3aa1ac0839323b9a52767a101dd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647043"
---
# <a name="certificate-and-trust-return-values"></a>Valores de retorno de certificado e de confiança

A tabela a seguir lista os valores de retorno de confiança do certificado e do certificado. Esses valores estão contidos no arquivo de cabeçalho Winerror. h.



| Nome                            | Descrição                                                                                                                    | Valor      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERTIFICADO \_ E \_ crítico               | Um certificado contém uma extensão desconhecida que está marcada como "crítica".                                                         | 0x800B0105 |
| \_ \_ nome inválido do certificado E \_          | O certificado tem um nome que não é válido. O nome não está incluído na lista de permissão ou foi excluído explicitamente. | 0x800B0114 |
| política de certificado \_ E \_ inválido \_        | O certificado tem uma política que não é válida.                                                                                | 0x800B0113 |
| CERTIFICADO \_ E \_ ISSUERCHAINING         | Um pai de um determinado certificado, de fato, não emitiu esse certificado filho.                                                  | 0x800B0107 |
| CERTIFICADO \_ E \_ mal formado              | Um certificado está ausente ou tem um valor vazio para um campo importante, como um assunto ou nome do emissor.                       | 0x800B0108 |
| CERTIFICADO \_ E \_ PATHLENCONST           | Uma restrição de tamanho de caminho na cadeia de certificação foi violada.                                                         | 0x800B0104 |
| CERTIFICADO \_ E \_ UNTRUSTEDCA            | Uma cadeia de certificação foi processada corretamente, mas um dos certificados de autoridade de certificação não é confiável pelo provedor de política.               | 0x800B0112 |
| Não CRIPTOGRAFAdo \_ E \_ nenhuma \_ verificação de revogação \_ | A função de revogação não pôde verificar a revogação do certificado.                                                    | 0x80092012 |
| CONFIAR \_ E \_ má \_ Digest           | A assinatura digital do objeto não foi verificada.                                                                            | 0x80096010 |
| CONFIANÇA \_ E \_ \_ restrições básicas    | A extensão de restrição básica de um certificado não foi observada.                                                         | 0x80096019 |
| CONFIANÇA \_ E \_ assinatura de certificado \_       | A assinatura do certificado não pode ser verificada.                                                                           | 0x80096004 |
| CONFIAR \_ no \_ \_ assinante E contador       | Uma das assinaturas do contador não era válida.                                                                                   | 0x80096003 |
| CONFIAR \_ E não confie \_ explícito \_    | O certificado foi explicitamente marcado como não confiável pelo usuário.                                                                | 0x800B0111 |
| \_ \_ critérios financeiros E de confiança \_   | O certificado não atende ou contém as extensões financeiras Authenticode.                                                | 0x8009601E |
| CONFIAR \_ E \_ nenhum \_ certificado de signatário \_      | O certificado para o signatário da mensagem não é válido ou não foi encontrado.                                                       | 0x80096002 |
| \_erro de \_ sistema confiável E \_         | Erro no sistema ao verificar a relação de confiança.                                                                           | 0x80096001 |
| \_carimbo de \_ Data E hora de confiança \_           | A assinatura do carimbo de data/hora ou o certificado não pôde ser verificado ou está malformado.                                                 | 0x80096005 |



 

 

 



