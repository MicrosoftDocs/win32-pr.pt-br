---
description: Os dados protegidos são armazenados como um BLOB codificado em ASN.1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de dados protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907398"
---
# <a name="protected-data-format"></a>Formato de dados protegidos

Os dados protegidos são armazenados como um BLOB codificado em ASN.1. Os dados são formatados como conteúdo envelocado de CMS (sintaxe de mensagem de certificado). O envelope digital contém conteúdo criptografado, informações de destinatário que contém uma CEK (chave de criptografia de conteúdo criptografado) e um título que contém informações sobre o conteúdo, incluindo a cadeia de caracteres de regra do descritor de proteção não criptografada. Isso é mostrado pelo diagrama a seguir.

![dados envelopes protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Descritores de proteção](protection-descriptors.md)
</dt> <dt>

[Provedores de proteção](protection-providers.md)
</dt> </dl>

 

 



