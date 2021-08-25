---
title: Cadeias de caracteres inseridas
description: As estruturas de informações não conterão cadeias de caracteres inseridas. Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas funções principais.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6121e805a1dbe329cee52a760c809ded21f1740b19adaa3e18eaa5033fd15897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912246"
---
# <a name="embedded-strings"></a>Cadeias de caracteres inseridas

As estruturas de informações não conterão cadeias de caracteres inseridas. Isso melhora o alinhamento das estruturas de informações e permite a flexibilidade do OEM nas funções principais.

Qualquer campo de informações retornado em uma chamada de enumeração que possa ser usada posteriormente como uma chave para a chamada a uma função de gerenciamento de rede GetInfo tem a garantia de estar presente no buffer de enumeração. Se a cadeia de caracteres de informações de comprimento variável que especificar o valor do campo de chave não se ajustar, toda a estrutura de comprimento fixo para a entrada não será retornada. Outros campos de comprimento variável serão retornados como um **ponteiro NULL** para o caso em que a cadeia de caracteres não se ajustar.

 

 




