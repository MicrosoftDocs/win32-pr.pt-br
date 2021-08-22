---
description: No Monitor de Rede, o filtro de captura é definido pela estrutura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: A estrutura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5c6d8d8f8baa3710b7dff4e33c98eb8791a65dc76931caa9068bbc1280f33e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339356"
---
# <a name="the-capturefilter-structure"></a>A estrutura CAPTUREFILTER

No Monitor de Rede, o [filtro de captura](capture-filters.md) é definido pela [**estrutura CAPTUREFILTER.**](capturefilter.md) A ausência ou combinação de sinalizadores, valores e expressões determina quais quadros serão passados ou descartados pelo driver Monitor de Rede. A ilustração a seguir mostra as três áreas da análise de filtro de captura: Etype/SAP, endereço e combinação de padrões.

![três áreas da análise de filtro de captura](images/capfilter.png)

A tabela a seguir lista a função de cada elemento de filtro de captura.



| Elemento Filter                                       | Ação                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etype/SAP](writing-etypesap-filter-portion.md)     | Avalia as configurações de Etype/SAP. A combinação de sinalizadores determina quais tipos de configuração ou valores são incluídos ou excluídos.                                                                                    |
| [Endereço](writing-addresstable-filter-portion.md)   | Avalia endereços de origem e destino e pares de endereços. Combinações diferentes de sinalizadores determinam quais valores individuais ou combinações de pares de endereços são incluídos ou excluídos.                   |
| [Corresponder ao padrão](writing-the-patternmatch-filter.md) | Define as correspondeções de padrão complexas dentro de um quadro. Sinalizadores são fornecidos para diferentes tipos e deslocamentos. Você pode combinar as correspondeções de padrão com instruções lógicas de operador AND ou OR.                              |
| [Recortando](clipping-a-frame.md)                     | Clipes de quadros de uma maneira especificada por vários valores de byte. Você pode usar apenas esse elemento para cortar todos os quadros ou usá-lo com outros elementos de filtro de captura; por exemplo, para encontrar e, em seguida, cortar um único quadro. |
| [**Gatilho**](trigger.md)                           | Esse elemento de filtro de captura está obsoleto. Os gatilhos não fazem mais parte de um filtro de captura; agora eles estão contidos em suas próprias marcas BLOB, que são especificadas separadamente.                                     |



 

Um quadro é avaliado em relação a todas as três partes do filtro de captura. Portanto, um quadro transmitido com êxito deve passar cada elemento. Esteja ciente de que Monitor de Rede driver de Monitor de Rede avalia a ausência de qualquer um dos três elementos como **TRUE.** Por exemplo, o driver avalia a ausência de uma seção Etype/SAP como "Todos os quadros com o valor ANY Etype/SAP são válidos".

 

 



