---
description: Quando o sistema inicia um programa que usa vinculação dinâmica em tempo de carregamento, ele usa as informações que o vinculador colocou no arquivo para localizar os nomes das DLLs usadas pelo processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506181"
---
# <a name="load-time-dynamic-linking"></a>Load-Time vinculação dinâmica

Quando o sistema inicia um programa que usa vinculação dinâmica em tempo de carregamento, ele usa as informações que o vinculador colocou no arquivo para localizar os nomes das DLLs usadas pelo processo. Em seguida, o sistema pesquisa as DLLs. Para obter mais informações, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md).

Se o sistema não puder localizar uma DLL necessária, ele encerrará o processo e exibirá uma caixa de diálogo que reportará o erro para o usuário. Caso contrário, o sistema mapeia a DLL para o espaço de endereço virtual do processo e incrementa a contagem de referência de DLL.

O sistema chama a função de ponto de entrada. A função recebe um código que indica que o processo está carregando a DLL. Se a função de ponto de entrada não retornar TRUE, o sistema encerrará o processo e relatará o erro. Para obter mais informações sobre a função de ponto de entrada, consulte [biblioteca de vínculo dinâmico Entry-Point função](dynamic-link-library-entry-point-function.md).

Por fim, o sistema modifica a tabela de endereços de função com os endereços iniciais para as funções de DLL importadas.

A DLL é mapeada para o espaço de endereço virtual do processo durante sua inicialização e é carregada na memória física somente quando necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Load-Time vinculação dinâmica](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



