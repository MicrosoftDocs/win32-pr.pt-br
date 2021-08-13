---
description: Quando o sistema inicia um programa que usa a vinculação dinâmica de tempo de carregamento, ele usa as informações que o linker colocou no arquivo para localizar os nomes das DLLs que são usadas pelo processo.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0adac32841d822bba67031dd79171c52f25d8308b055aee2c55bb804ebefe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649354"
---
# <a name="load-time-dynamic-linking"></a>Load-Time vinculação dinâmica

Quando o sistema inicia um programa que usa a vinculação dinâmica de tempo de carregamento, ele usa as informações que o linker colocou no arquivo para localizar os nomes das DLLs que são usadas pelo processo. Em seguida, o sistema pesquisa as DLLs. Para obter mais informações, consulte [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

Se o sistema não puder localizar uma DLL necessária, ele encerrará o processo e exibirá uma caixa de diálogo que relata o erro ao usuário. Caso contrário, o sistema mapeia a DLL para o espaço de endereço virtual do processo e incrementa a contagem de referência de DLL.

O sistema chama a função de ponto de entrada. A função recebe um código que indica que o processo está carregando a DLL. Se a função de ponto de entrada não retornar TRUE, o sistema encerrará o processo e relata o erro. Para obter mais informações sobre a função de ponto de entrada, consulte [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).

Por fim, o sistema modifica a tabela de endereços de função com os endereços in básicas para as funções de DLL importadas.

A DLL é mapeada para o espaço de endereço virtual do processo durante sua inicialização e é carregada na memória física somente quando necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Load-Time vinculação dinâmica](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



