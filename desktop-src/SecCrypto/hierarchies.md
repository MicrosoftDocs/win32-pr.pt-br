---
description: Os serviços de certificados oferecem suporte a hierarquias de autoridade de certificação (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarquias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754600"
---
# <a name="hierarchies"></a>Hierarquias

Os serviços de certificados oferecem suporte a hierarquias de [*autoridade de certificação*](../secgloss/c-gly.md) (CA). Uma [*hierarquia de CA*](../secgloss/c-gly.md) consiste em uma autoridade de certificação de nível superior (chamada de CA raiz) com uma ou mais CAS subordinadas que receberam certificados pela autoridade de certificação raiz. Um cenário de hierarquia de autoridade de certificação pode estar em uma organização com uma AC raiz, que foi usada para emitir certificados para várias CAs subordinadas. As CAs subordinadas podem emitir certificados de entidade final, como certificados emitidos para um usuário. O certificado do usuário conterá um caminho de confiança para a hierarquia da autoridade de certificação, nesse caso, incluindo o certificado para a AC subordinada emissora, bem como a autoridade de certificação raiz.

 

 
