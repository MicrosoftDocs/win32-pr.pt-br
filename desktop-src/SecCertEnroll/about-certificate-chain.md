---
description: Uma cadeia de certificados é uma coleção hierárquica de certificados que leva do usuário final ou computador de volta para uma raiz de confiança, normalmente a CA (autoridade de certificação) raiz de uma organização.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Cadeia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756690"
---
# <a name="certificate-chain"></a>Cadeia de certificados

Uma cadeia de certificados é uma coleção hierárquica de certificados que leva do usuário final ou computador de volta para uma raiz de confiança, normalmente a CA (autoridade de certificação) raiz de uma organização. Como todas as partes supostamente confiam no certificado raiz, uma parte pode obter confiança em um certificado de entidade final, verificando a cadeia de certificados. A verificação normalmente requer o estabelecimento de cada certificado na cadeia:

-   É assinado pela chave pública no certificado anterior.
-   Não expirou.
-   Não foi revogado.
-   Está de acordo com as políticas especificadas pelos certificados anteriores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hierarquia de certificados](about-certificate-hierarchy.md)
</dt> <dt>

[Certificação cruzada](about-cross-certification.md)
</dt> <dt>

[Modelos de confiança](about-trust-models.md)
</dt> </dl>

 

 



