---
description: Os exemplos a seguir mostram algumas expressões regulares manuscritas que você pode criar.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Exemplos de expressões regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe207be6378754bfe4b3e504d51e6ff49cadba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808333"
---
# <a name="regular-expression-examples"></a>Exemplos de expressões regulares

Os exemplos a seguir mostram algumas expressões regulares manuscritas que você pode criar.



| Expression                                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                               | Corresponde a                                                                          | Não correspondências                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s (! é \_ ONECHAR) + p<br/>                                                                                                                                                                                                                                                                | Faz a correspondência de qualquer palavra que comece com letras minúsculas, contém um ou mais caracteres (conforme definido pelo \_ escopo de entrada is ONECHAR) e termina com um "p" minúsculo.<br/> | parar<br/> sopa<br/> schlep<br/> s234p<br/>               | Stop<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Corresponde a qualquer dígito único, 1 a 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Um<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -) +<br/>                                                                                                                                                                                                                                            | Corresponde a um ou mais dígitos, vírgulas ou traços únicos. Útil para limitar a entrada a um intervalo ou conjunto de números, como um intervalo de páginas a ser impresso.<br/>               | 1<br/> 1-6<br/> 2, 4, 7<br/> 2-6, 9135<br/> ,,,<br/> | Três<br/> 7 a 9<br/>   |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/> | Um número do seguro social. O formato de um número de seguro social é *nnn*  -  *NN*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




