---
description: O tipo de dados de data/hora tem a hora e a data armazenadas individualmente, usando inteiros não assinados como campos de bits, compactados da seguinte maneira.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Data/hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748565"
---
# <a name="timedate"></a>Data/hora

O tipo de dados de data/hora tem a hora e a data armazenadas individualmente, usando inteiros não assinados como campos de bits, compactados da seguinte maneira.

## <a name="time"></a>Hora

O tempo é codificado em um inteiro sem sinal de 2 bytes com os campos de bits a seguir.



| Sumário           | Bits        | Intervalo de valor |
|--------------------|-------------|-------------|
| horas              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| intervalos de 2 segundos | B C D E F   | 0 – 29        |



 

## <a name="date"></a>Data

A data é codificada em um inteiro sem sinal de 2 bytes com os campos de bits a seguir.



| Sumário | Bits          | Intervalo de valor              |
|----------|---------------|--------------------------|
| ano     | 0 1 2 3 4 5 6 | 0 – 119 (relativa a 1980) |
| mês    | 7 8 9 A       | 1–12                     |
| dia      | B C D E F     | 1–31                     |



 

 

 



