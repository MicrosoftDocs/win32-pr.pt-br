---
title: Atributos de ACF de gerenciamento de memória
description: Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- MIDL de ACF, atributos, gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917249"
---
# <a name="memory-management-acf-attributes"></a>Atributos de ACF de gerenciamento de memória

Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.



| Atributo                                   | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**aloca**](allocate.md)                | Especifica a maneira como o aplicativo cliente e o stub alocam e liberam memória para ponteiros. Esse atributo é particularmente útil quando você deseja que determinadas estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor após a chamada de procedimento remoto retornar ao cliente. Você também pode usar o atributo [**ALLOCATE**](allocate.md) para direcionar o stub para calcular o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada para o [**usuário de MIDL \_ \_ alocar**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**contagem de bytes \_**](byte-count.md)           | Permite que você crie um bloco persistente e contíguo de memória que pode ser reutilizado em várias chamadas de procedimento remoto. Isso libera o aplicativo cliente da sobrecarga de alocar repetidamente e liberar memória que pode incluir vários ponteiros e outras estruturas de dados complexas.                                                                                                                                                                                                                                                      |
| [**Habilitar \_ alocação**](enable-allocate.md) | Especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 