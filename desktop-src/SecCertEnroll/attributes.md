---
description: Atributos (API de registro de certificado)-os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Atributos (API de registro de certificado)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aec93ec47a700902cb1275e25af6649e6988b76f7204b01487249e0130dd35b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903098"
---
# <a name="attributes-certificate-enrollment-api"></a>Atributos (API de registro de certificado)

Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado. cada atributo é uma estrutura ASN (authorized. 1 [*) codificada*](/windows/desktop/SecGloss/a-gly) de [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) que contém um OID (identificador de objeto) e zero ou mais valores. Os atributos são definidos usando interfaces incluídas com a API de registro de certificado. Os tópicos a seguir abordam os atributos mais detalhadamente:

-   [Atributos com suporte](supported-attributes.md)
-   [Arquitetura de atributo](attribute-architecture.md)
-   [\#Atributos PKCS 7](pkcs--7-attributes.md)
-   [\#Atributos PKCS 10](pkcs--10-attributes.md)
-   [Atributos CMC](cmc-attributes.md)

 

 
