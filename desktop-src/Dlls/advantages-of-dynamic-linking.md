---
description: A vinculação dinâmica tem as seguintes vantagens em relação à vinculação estática.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vantagens da vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780549"
---
# <a name="advantages-of-dynamic-linking"></a>Vantagens da vinculação dinâmica

A vinculação dinâmica tem as seguintes vantagens em relação à vinculação estática:

-   Vários processos que carregam a mesma DLL no mesmo endereço base compartilham uma única cópia da DLL na memória física. Isso poupa a memória do sistema e reduz a permuta.
-   Quando as funções em uma DLL são alteradas, os aplicativos que as usam não precisam ser recompilados ou vinculados desde que os argumentos da função, convenções de chamada e valores de retorno não sejam alterados. Por outro lado, o código do objeto vinculado estaticamente requer que o aplicativo seja vinculado novamente quando as funções forem alteradas.
-   Uma DLL pode fornecer suporte após o mercado. Por exemplo, uma DLL de driver de vídeo pode ser modificada para dar suporte a uma exibição que não estava disponível quando o aplicativo foi lançado inicialmente.
-   Programas escritos em linguagens de programação diferentes podem chamar a mesma função de DLL, desde que os programas sigam a mesma convenção de chamada usada pela função. A Convenção de chamada (como C, Pascal ou chamada padrão) controla a ordem na qual a função de chamada deve enviar os argumentos para a pilha, se a função ou a função de chamada é responsável por limpar a pilha e se os argumentos são passados em registros. Para obter mais informações, consulte a documentação incluída no seu compilador.

Uma desvantagem potencial de usar DLLs é que o aplicativo não é independente; depende da existência de um módulo DLL separado. O sistema encerra os processos usando a vinculação dinâmica em tempo de carregamento se eles exigem uma DLL que não foi encontrada na inicialização do processo e fornece uma mensagem de erro ao usuário. O sistema não encerra um processo usando vinculação dinâmica em tempo de execução nessa situação, mas as funções exportadas pela DLL ausente não estão disponíveis para o programa.

 

 



