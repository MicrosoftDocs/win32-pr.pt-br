---
description: O tipo de dados Time/Date tem a hora e a data armazenadas individualmente, usando inteiros sem sinal como campos de bits, empacotados da seguinte maneira.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Hora/data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3c5cccc2f1211918b52008f0d81a7e4693dfd14766696b77cd184d75f4309d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810736"
---
# <a name="timedate"></a>Hora/data

O tipo de dados Time/Date tem a hora e a data armazenadas individualmente, usando inteiros sem sinal como campos de bits, empacotados da seguinte maneira.

## <a name="time"></a>Tempo

O tempo é codificado em um inteiro sem sinal de 2 byte com os campos de bits a seguir.



| Sumário           | Bits        | Intervalo de valor |
|--------------------|-------------|-------------|
| horas              | 0 1 2 3 4   | 0–23        |
| minutes            | 5 6 7 8 9 A | 0–59        |
| Intervalos de 2 segundos | B C D E F   | 0–29        |



 

## <a name="date"></a>Data

Date é codificado em um inteiro de 2 byte sem sinal com os campos de bits a seguir.



| Sumário | Bits          | Intervalo de valor              |
|----------|---------------|--------------------------|
| ano     | 0 1 2 3 4 5 6 | 0–119 (relativo a 1980) |
| mês    | 7 8 9 A       | 1–12                     |
| dia      | B C D E F     | 1–31                     |



 

 

 



