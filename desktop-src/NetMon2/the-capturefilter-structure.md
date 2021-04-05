---
description: No Monitor de Rede, o filtro de captura é definido pela estrutura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: A estrutura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920992"
---
# <a name="the-capturefilter-structure"></a>A estrutura CAPTUREFILTER

No Monitor de Rede, o [filtro de captura](capture-filters.md) é definido pela estrutura [**CAPTUREFILTER**](capturefilter.md) . A ausência ou a combinação de sinalizadores, valores e expressões determina quais quadros serão passados ou descartados pelo driver de Monitor de Rede. A ilustração a seguir mostra as três áreas da análise do filtro de captura: ETYPE/SAP, endereço e correspondência de padrão.

![três áreas da análise do filtro de captura](images/capfilter.png)

A tabela a seguir lista a função de cada elemento de filtro de captura.



| Elemento Filter                                       | Ação                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ETYPE/SAP](writing-etypesap-filter-portion.md)     | Avalia as configurações de ETYPE/SAP. A combinação de sinalizadores determina quais tipos de configuração ou valores são incluídos ou excluídos.                                                                                    |
| [Endereço](writing-addresstable-filter-portion.md)   | Avalia os endereços de origem e de destino e os pares de endereços. Diferentes combinações de sinalizadores determinam quais valores individuais ou combinações de pares de endereços são incluídos ou excluídos.                   |
| [Correspondência de padrões](writing-the-patternmatch-filter.md) | Define correspondências de padrão complexas dentro de um quadro. Os sinalizadores são fornecidos para diferentes tipos e deslocamentos. Você pode combinar correspondências de padrão com instruções lógicos AND ou OR Operator.                              |
| [Recorte](clipping-a-frame.md)                     | Corta os quadros de uma maneira especificada por vários valores de byte. Você pode usar somente esse elemento para recortar todos os quadros ou usá-los com outros elementos de filtro de captura; por exemplo, para localizar e recortar um único quadro. |
| [**Of**](trigger.md)                           | Este elemento de filtro de captura está obsoleto. Os gatilhos não fazem mais parte de um filtro de captura; Agora eles estão contidos em suas próprias marcas de BLOB, que são especificadas separadamente.                                     |



 

Um quadro é avaliado em relação a todas as três partes do filtro de captura. Portanto, um quadro transmitido com êxito deve passar cada elemento. Lembre-se de que o driver Monitor de Rede avalia a ausência de qualquer um dos três elementos como **verdadeiro**. Por exemplo, o driver avalia a ausência de uma seção ETYPE/SAP como "todos os quadros com qualquer valor de ETYPE/SAP são válidos".

 

 



