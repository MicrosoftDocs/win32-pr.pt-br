---
description: A certificação cruzada permite que entidades em uma PKI (infraestrutura de chave pública) confiem em entidades em outra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificação cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644e5326f9d3b9f7cbe87290c044dea7f401f8a888fa3904afa162118a98d89b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904536"
---
# <a name="cross-certification"></a>Certificação cruzada

A certificação cruzada permite que entidades em uma PKI (infraestrutura de chave pública) confiem em entidades em outra PKI. Essa relação de confiança mútua normalmente é suportada por um contrato de certificação cruzada entre as autoridades de certificação (CAs) em cada PKI. O contrato estabelece as responsabilidades e a responsabilidade de cada parte.

Uma relação de confiança mútua entre duas AAs requer que cada AC em emitido um certificado para o outro estabeleça a relação em ambas as direções. O caminho de confiança não é hierarquica (nenhuma das AAs que regem é subordinada à outra), embora os PKIs separados possam ser hierarquias de certificado. Depois que duas AAs estabelecerem e especificarem os termos de confiança e os certificados emitidos entre si, as entidades dentro dos PKIs separados poderão interagir sujeitos às políticas especificadas nos certificados.

![diagrama de certificação cruzada](images/cross-certification.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de confiança](about-trust-models.md)
</dt> </dl>

 

 



