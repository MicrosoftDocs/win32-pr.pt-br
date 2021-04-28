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
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118424"
---
# <a name="attributes-certificate-enrollment-api"></a>Atributos (API de registro de certificado)

Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado. Cada atributo é uma estrutura ASN (Authorized. 1 [*) codificada*](/windows/desktop/SecGloss/a-gly) de [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) que contém um OID (identificador de objeto) e zero ou mais valores. Os atributos são definidos usando interfaces incluídas com a API de registro de certificado. Os tópicos a seguir abordam os atributos mais detalhadamente:

-   [Atributos com suporte](supported-attributes.md)
-   [Arquitetura de atributo](attribute-architecture.md)
-   [\#Atributos PKCS 7](pkcs--7-attributes.md)
-   [\#Atributos PKCS 10](pkcs--10-attributes.md)
-   [Atributos CMC](cmc-attributes.md)

 

 
