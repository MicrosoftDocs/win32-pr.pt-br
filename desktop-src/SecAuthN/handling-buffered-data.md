---
description: Várias das funções de provedor de rede pegam o endereço e o tamanho de um buffer no qual a função coloca uma estrutura de dados de tamanho variável.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Manipulando dados armazenados em buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170823"
---
# <a name="handling-buffered-data"></a>Manipulando dados armazenados em buffer

Várias das funções de provedor de rede pegam o endereço e o tamanho de um buffer no qual a função coloca uma estrutura de dados de tamanho variável.

Em cada caso, o mecanismo usado é o mesmo. O chamador aloca um buffer e passa seu endereço para a função. Ele também passa o endereço de um **DWORD** que especifica o tamanho do buffer, em bytes.

Em seguida, a função copia o máximo da estrutura de dados solicitada como pode no buffer. Se todos os dados couberem no buffer, a função retornará o sucesso de WN \_ . Se os dados não couberem no buffer, os dados poderão ficar incompletos e a função definirá o \_ erro de mais dados do WN \_ . Em ambos os casos, o **DWORD** que indica o tamanho do buffer é definido como o número de bytes realmente exigidos pela estrutura de dados. Dessa forma, se o buffer passado era muito pequeno e a função falhou, o chamador pode alocar um novo buffer do tamanho necessário e chamar a função novamente.

Quando as estruturas de dados retornadas incluem cadeias de caracteres de comprimento variável, as estruturas de dados individuais normalmente contêm ponteiros para essas cadeias de caracteres. As cadeias de caracteres em si também devem ser colocadas dentro do buffer. No entanto, é importante colocá-los no final do buffer. Caso contrário, eles tornarão a indexação a enésimo estrutura impossível. Em outras palavras, todas as estruturas estão localizadas de forma contígua no início do buffer. Ponteiros para cadeias de caracteres ou dados de comprimento variável devem ser ponteiros reais, não deslocamentos no buffer.

Quando um buffer é usado para passar e retornar dados que consistem apenas em cadeias de caracteres, o **DWORD** que especifica o tamanho do buffer deve ser definido como o número total de personagens que se ajustarão a essas cadeias, não ao número de bytes.

 

 



