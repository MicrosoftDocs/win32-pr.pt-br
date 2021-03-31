---
description: O provedor base original reportou incorretamente que o algoritmo de hash SHA enumerando algoritmos por chamadas para CryptGetProvParam com o parâmetro PP \_ ENUMALGS especificado.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funcionalidade de SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646664"
---
# <a name="sha-functionality"></a>Funcionalidade de SHA

O provedor base original reportou incorretamente que o algoritmo de hash [*Sha*](../secgloss/s-gly.md) enumerando algoritmos por chamadas para [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o parâmetro PP \_ ENUMALGS especificado. Isso foi corrigido no provedor base. O provedor base revisado e o provedor estendido e agora relatam corretamente o SHA-1.

Uma constante CALG \_ SHA1 definida foi adicionada a Wincrypt. h com o mesmo valor que CALG \_ Sha.

 

 
