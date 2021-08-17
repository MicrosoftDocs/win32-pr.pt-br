---
description: O provedor de base cria chaves simétricas de 40 bits criadas com onze bytes de Salt de zero valor, onze bytes de Salt diferente de zero se cript. \_ Create \_ Salt for especificado ou nenhum valor de Salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funcionalidade de valor de Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f911815152861921f1ffe12090c88ad4795ba042346aee875138acf591d14671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900366"
---
# <a name="salt-value-functionality"></a>Funcionalidade de valor de Salt

O provedor de base cria [*chaves simétricas*](../secgloss/s-gly.md) de 40 bits criadas com onze bytes de [*Salt*](../secgloss/s-gly.md)de zero valor, onze bytes de Salt diferente de zero se cript. \_ Create \_ Salt for especificado ou nenhum valor de Salt. No entanto, uma chave simétrica de 40 bits com Salt de valor zero não é equivalente a uma chave simétrica de 40 bits sem Salt. Para interoperabilidade, as chaves devem ser criadas sem Salt. Esse problema resulta de uma condição padrão que ocorre apenas com chaves de exatamente 40 bits. Todos os outros [*comprimentos de chave*](../secgloss/k-gly.md) não têm Salt alocado por padrão.

Tanto os provedores de base quanto o provedor estendido podem usar o \_ sinalizador de Salt não criptografado \_ para especificar que nenhum valor de Salt seja alocado para uma chave simétrica de 40 bits. As funções que aceitam esse sinalizador são [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Por padrão, essas funções fornecem compatibilidade com versões anteriores para o caso de chave simétrica de 40 bits, continuando o uso do Salt de onze bytes de valor zero.

 

 
