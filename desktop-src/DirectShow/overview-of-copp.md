---
description: Visão geral de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Visão geral de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779838"
---
# <a name="overview-of-copp"></a>Visão geral de COPP

Aqui estão as etapas básicas que um aplicativo deve executar para usar o protocolo de proteção de saída certificado (COPP).

**Obter a cadeia de certificados do driver**

1.  Crie um grafo de reprodução do DirectShow que renderiza o vídeo usando o processador de mixagem de vídeo (VMR-7 ou VMR-9) ou o filtro de [**processador de vídeo aprimorado**](enhanced-video-renderer-filter.md) (EVR).
2.  Consulte o VMR para a interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .
3.  Chame [**IAMCertifiedOutputProtection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Esse método retorna um número aleatório de 128 bits do driver, juntamente com uma cadeia de certificados que contém a chave pública RSA de 2048 bits do driver.

**Validar a cadeia de certificados**

1.  Valide a cadeia de certificados. Se a cadeia de certificados não for válida, pare.
2.  Verifique a CRL (lista de certificados revogados). Se qualquer um dos certificados na cadeia de certificados aparecer na lista de revogação, pare.
3.  Obtenha a chave pública RSA da cadeia de certificados.

**Inicializar a sessão COPP**

1.  Gere uma chave de sessão AES de 128 bits. Essa chave é usada para assinar dados e verificar se os dados assinados não foram adulterados.
2.  Gere dois números aleatórios de 32 bits seguros criptograficamente. O primeiro é um número de sequência de status e o segundo é um número de sequência de comando. Cada vez que o aplicativo envia um comando ou uma solicitação de status, ele incrementa o número de sequência correspondente e inclui esse número no comando COPP ou nos dados de solicitação.
3.  Concatene o número aleatório de 128 bits do driver de gráficos, a chave de sessão AES, o número de sequência de status e o número de sequência de comando. Criptografe esta matriz de bytes usando a chave pública do driver e passe o resultado para [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**Enviar comandos COPP e solicitações de status**

1.  Consulte os tipos de proteção disponíveis e outras informações chamando [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).
2.  Defina os níveis de proteção desejados chamando [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).
3.  Consulte periodicamente o nível de proteção local atual. Pare a reprodução se o nível de proteção local for alterado inesperadamente ou se um problema for detectado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



