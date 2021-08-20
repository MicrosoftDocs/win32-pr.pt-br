---
description: ICE81 valida a tabela MsiDigitalCertificate, a tabela MsiDigitalSignature, a tabela MsiPatchCertificate e a tabela MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bcf3228282339acd76ae4f20638cc24aeddf5279212b91aca0ece2b21867d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580806"
---
# <a name="ice81"></a>ICE81

ICE81 valida a tabela [MsiDigitalCertificate](msidigitalcertificate-table.md), a tabela [MsiDigitalSignature](msidigitalsignature-table.md), a [tabela MsiPatchCertificate](msipatchcertificate-table.md)e a [tabela MsiPackageCertificate](msipackagecertificate-table.md). Essa ação personalizada ice posta avisos para certificados digitais que não são usado ou não são deferência e posta um erro quando o objeto assinado não existe ou quando o gabinete do objeto assinado não aponta para dados externos.

Observe que ICE03 verifica se a entrada na coluna Tabela na tabela MsiDigitalSignature é "Media".

## <a name="result"></a>Resultado

O ICE81 posta os avisos a seguir para certificados digitais não ou nãoferenciados.



| Aviso ICE81                                                                                                                                                      | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Nenhuma referência a nenhum dos registros na tabela MsiDigitalCertificate pode ser encontrada nas tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate. | Esse aviso será retornado se todos os registros não tiverem uso.                |
| Nenhuma referência ao Certificado Digital 1 pode ser encontrada nas \[ \] tabelas MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.                         | Esse aviso será retornado se alguns registros, mas não todos, não tiverem uso. |



 

ICE81 posta os seguintes erros.



| Erro ICE81                                                                                                                                                              | Descrição                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A Tabela de Mídia não existe. Portanto, todas as entradas em MsiDigitalSignature estão incorretas                                                                                   | O objeto assinado não existe. Esse erro será retornado se a tabela Media não existir, mas MsiDigitalSignature tiver entradas.                                |
| Objeto assinado \[ ausente 2 \] na Tabela de Mídia                                                                                                                               | O objeto assinado \[ 2 \] não existe. Esse erro será retornado se a tabela Mídia existir, mas essa entrada em MsiDigitalSignature não está presente na tabela Mídia. |
| A entrada na tabela \[ 1 \] com a chave \[ 2 está \] assinada. Portanto, o gabinete deve apontar para um objeto fora do pacote (o valor de Gabinete NÃO deve ser prefixado com \# ) | O gabinete do objeto assinado não aponta para dados externos. \[1 \] é o nome da tabela. \[2 \] é a chave na tabela Mídia.                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



