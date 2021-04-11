---
description: Os dados protegidos são armazenados como um BLOB codificado ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de dados protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091446"
---
# <a name="protected-data-format"></a>Formato de dados protegidos

Os dados protegidos são armazenados como um BLOB codificado ASN. 1. Os dados são formatados como conteúdo envelopado do CMS (sintaxe de mensagem de certificado). O envelope digital contém conteúdo criptografado, informações do destinatário que contêm uma chave de criptografia de conteúdo criptografado (CEK) e um cabeçalho que contém informações sobre o conteúdo, incluindo a cadeia de caracteres da regra de descritor de proteção não criptografada. Isso é mostrado pelo diagrama a seguir.

![dados de envelope protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[Descritores de proteção](protection-descriptors.md)
</dt> <dt>

[Provedores de proteção](protection-providers.md)
</dt> </dl>

 

 



