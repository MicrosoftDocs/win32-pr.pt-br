---
description: As estruturas de dados usadas pelo TSPI são idênticas àquelas definidas nas estruturas TAPI, com exceção de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estruturas TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758110"
---
# <a name="tspi-structures"></a>Estruturas TSPI

As estruturas de dados usadas pelo TSPI são idênticas àquelas definidas nas [estruturas TAPI](./tapi-structures.md), com exceção de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

No caso da maioria das estruturas de dados maiores, a responsabilidade pelo preenchimento de membros é dividida entre o provedor de serviços e a TAPI. O provedor de serviços deve preservar os valores presentes nos membros de propriedade da TAPI. A descrição de quais membros devem ser definidos pelo provedor de serviços e que deve ser preservada é fornecida na seção funções nas funções que se referem a essa estrutura de dados.

Para cada estrutura, a seção de referência lista os seguintes itens:

-   A finalidade da estrutura
-   Uma descrição dos valores ou campos
-   Uma descrição da extensibilidade da estrutura
-   Comentários opcionais sobre como usar a estrutura
-   Referências opcionais a outras funções, mensagens, constantes ou estruturas.

Memória para todas as estruturas de dados cuja representação é publicada e compartilhada pela TAPI e o provedor de serviços é alocado pela TAPI ou por um aplicativo que usa a TAPI. A TAPI passa um ponteiro para a função TSPI que retorna as informações. TSPI preenche a estrutura de dados com as informações solicitadas. Se a operação for assíncrona, as informações não estarão disponíveis até que o retorno de chamada de resposta assíncrona indique êxito.

> [!Note]  
> Algumas estruturas incluem campos de tamanho e deslocamento para definir o local e o comprimento das cadeias de caracteres na parte variável da estrutura. Se o provedor de serviços for solicitado a adicionar uma cadeia de caracteres, mas nenhuma cadeia de caracteres estiver disponível, o provedor de serviços deverá indicar essa condição de uma das seguintes maneiras:
>
> -   Defina os campos tamanho e deslocamento como 0.
> -   Defina o campo de deslocamento para zero, mas o tamanho como 0.
> -   Defina o campo de deslocamento como diferente de zero, o tamanho como 1 e o byte no deslocamento como 0.

 

 

 
