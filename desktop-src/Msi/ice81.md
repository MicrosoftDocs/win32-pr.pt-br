---
description: ICE81 valida a tabela MsiDigitalCertificate, a tabela MsiDigitalSignature, a tabela MsiPatchCertificate e a tabela MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647472"
---
# <a name="ice81"></a>ICE81

ICE81 valida a tabela [MsiDigitalCertificate](msidigitalcertificate-table.md), a [tabela MsiDigitalSignature](msidigitalsignature-table.md), a tabela [MsiPatchCertificate](msipatchcertificate-table.md)e a [tabela MsiPackageCertificate](msipackagecertificate-table.md). Essa ação personalizada de ICE posta avisos para certificados digitais que não são usados ou não referenciados e posta um erro quando o objeto assinado não existe ou quando o gabinete do objeto assinado não aponta para dados externos.

Observe que ICE03 verifica se a entrada na coluna Table na tabela MsiDigitalSignature é "Media".

## <a name="result"></a>Resultado

ICE81 posta os seguintes avisos para certificados digitais não utilizados ou não referenciados.



| Aviso de ICE81                                                                                                                                                      | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Nenhuma referência a nenhum dos registros na tabela MsiDigitalCertificate foi encontrada nas tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate. | Esse aviso será retornado se todos os registros estiverem inutilizados.                |
| Nenhuma referência ao certificado digital \[ 1 \] foi encontrada nas tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.                         | Esse aviso será retornado se alguns registros, mas não todos, não forem usados. |



 

ICE81 posta os erros a seguir.



| Erro de ICE81                                                                                                                                                              | Descrição                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A tabela de mídia não existe. Portanto, todas as entradas em MsiDigitalSignature estão incorretas                                                                                   | O objeto assinado não existe. Esse erro será retornado se a tabela de mídia não existir, mas MsiDigitalSignature tiver entradas.                                |
| Objeto assinado \[ 2 ausente \] na tabela de mídia                                                                                                                               | O objeto assinado \[ 2 \] não existe. Esse erro será retornado se a tabela de mídia existir, mas essa entrada em MsiDigitalSignature não estiver presente na tabela de mídia. |
| A entrada na tabela \[ 1 \] com a chave \[ 2 \] é assinada. Portanto, o gabinete deve apontar para um objeto fora do pacote (o valor do gabinete não deve ser prefixado \# ) | O gabinete do objeto assinado não aponta para dados externos. \[1 \] é o nome da tabela. \[2 \] é a chave na tabela de mídia.                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



