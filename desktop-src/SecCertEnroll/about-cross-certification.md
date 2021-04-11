---
description: A certificação cruzada habilita entidades em uma PKI (infraestrutura de chave pública) para confiar em entidades em outra PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certificação cruzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170648"
---
# <a name="cross-certification"></a>Certificação cruzada

A certificação cruzada habilita entidades em uma PKI (infraestrutura de chave pública) para confiar em entidades em outra PKI. Essa relação de confiança mútua normalmente é suportada por um contrato de certificação cruzada entre as CAs (autoridades de certificação) em cada PKI. O contrato estabelece as responsabilidades e a responsabilidade de cada parte.

Uma relação de confiança mútua entre duas CAs requer que cada CA emita um certificado para o outro para estabelecer a relação em ambas as direções. O caminho de confiança não é hierárquico (nenhuma das CAs reguladoras é subordinada ao outro), embora as PKIs separadas possam ser hierarquias de certificado. Depois que duas CAs tiverem estabelecido e especificado os termos de confiança e os certificados emitidos entre si, as entidades dentro da PKIs separada poderão interagir com as políticas especificadas nos certificados.

![diagrama de certificação cruzada](images/cross-certification.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de confiança](about-trust-models.md)
</dt> </dl>

 

 



