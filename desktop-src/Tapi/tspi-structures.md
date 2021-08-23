---
description: As estruturas de dados que o TSPI usa são idênticas àquelas definidas em Estruturas TAPI, com exceção de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estruturas TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c11700dcaa46284b4050908ca70ed640e03afeb2eb7a2269ad1bac9161c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139749"
---
# <a name="tspi-structures"></a>Estruturas TSPI

As estruturas de dados que o TSPI usa são idênticas àquelas definidas em Estruturas [TAPI,](./tapi-structures.md)com exceção de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

No caso da maioria das estruturas de dados maiores, a responsabilidade de preencher membros é dividida entre o provedor de serviços e a TAPI. O provedor de serviços deve preservar os valores presentes em membros pertencentes à TAPI. A descrição de quais membros devem ser definidos pelo provedor de serviços e que devem ser preservados é fornecida na seção Funções nas funções que se referem a essa estrutura de dados.

Para cada estrutura, a seção de referência lista os seguintes itens:

-   A finalidade da estrutura
-   Uma descrição dos valores ou campos
-   Uma descrição da extensibilidade da estrutura
-   Comentários opcionais sobre como usar a estrutura
-   Referências opcionais a outras funções, mensagens, constantes ou estruturas.

A memória para todas as estruturas de dados cuja representação é publicada e compartilhada pela TAPI e pelo provedor de serviços é alocada pela TAPI ou por um aplicativo usando TAPI. TAPI passa um ponteiro para a função TSPI que retorna as informações. O TSPI preenche a estrutura de dados com as informações solicitadas. Se a operação for assíncrona, as informações não estarão disponíveis até que o retorno de chamada de resposta assíncrono indique êxito.

> [!Note]  
> Algumas estruturas incluem campos Tamanho e Deslocamento para definir o local e o comprimento das cadeias de caracteres na parte variável da estrutura. Se o provedor de serviços for solicitado a adicionar uma cadeia de caracteres, mas nenhuma cadeia de caracteres estiver disponível, o provedor de serviços deverá indicar essa condição de uma destas maneiras:
>
> -   De definir os campos Tamanho e Deslocamento como 0.
> -   De definir o campo Deslocamento como não zero, mas Tamanho como 0.
> -   De definir o campo Deslocamento como não zero, Tamanho como 1 e o byte no Deslocamento como 0.

 

 

 
