---
title: Cadeias de caracteres inseridas
description: As estruturas de informações não conterão cadeias de caracteres inseridas. Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas principais funções.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636261"
---
# <a name="embedded-strings"></a>Cadeias de caracteres inseridas

As estruturas de informações não conterão cadeias de caracteres inseridas. Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas principais funções.

Qualquer campo de informações retornado em uma chamada de enumeração que pode ser usado posteriormente como uma chave para a chamada para uma função de gerenciamento de rede GetInfo é garantido como presente no buffer de enumeração. Se a cadeia de caracteres de informações de comprimento variável que especificasse o valor do campo de chave não couber, toda a estrutura de comprimento fixo da entrada não será retornada. Outros campos de comprimento variável serão retornados como um ponteiro **NULL** para o caso em que a cadeia de caracteres não couber.

 

 




