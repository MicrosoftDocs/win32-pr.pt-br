---
description: Os Serviços de Certificados são compatíveis com hierarquias de AC (autoridade de certificação).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarquias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006294"
---
# <a name="hierarchies"></a>Hierarquias

Os Serviços de Certificados [*são compatíveis*](../secgloss/c-gly.md) com hierarquias de AC (autoridade de certificação). Uma [*hierarquia de*](../secgloss/c-gly.md) AC consiste em uma AC de nível superior (chamada ac raiz) com uma ou mais AC subordinadas que foram emitidas certificados pela AC raiz. Um cenário de hierarquia de AC possível estaria em uma organização com uma AC raiz, que foi usada para emitir certificados para várias AAs subordinadas. As AIs subordinadas podem emitir certificados de entidade final, como certificados emitidos para um usuário. O certificado do usuário conterá um caminho de confiança para a hierarquia de AC, nesse caso, incluindo o certificado para a AC subordinada em emissão, bem como a AC raiz.

 

 
