---
title: Atributos do ACF de gerenciamento de memória
description: Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL, atributos, gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d7df6f020d8531f0c1ca8bebdd6bf59270f2ed22c821e2c183c9da6936e306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013743"
---
# <a name="memory-management-acf-attributes"></a>Atributos do ACF de gerenciamento de memória

Os atributos listados na tabela a seguir permitem que você execute o gerenciamento de memória do lado do cliente.



| Atributo                                   | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Alocar**](allocate.md)                | Especifica a maneira como o aplicativo cliente e o stub alocam e liberam memória para ponteiros. Esse atributo é particularmente útil quando você deseja que determinadas estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor após a chamada de procedimento remoto retornar ao cliente. Você também pode usar o atributo [**allocate**](allocate.md) para direcionar o stub para calcular o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada ao usuário médio [**\_ \_ alocar**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**contagem de \_ byte**](byte-count.md)           | Permite que você crie um bloco persistente e contíguo de memória que pode ser reutilizado em várias chamadas de procedimento remoto. Isso libera o aplicativo cliente da sobrecarga de alocar e liberar repetidamente memória que pode incluir vários ponteiros e outras estruturas de dados complexas.                                                                                                                                                                                                                                                      |
| [**\_habilitar alocar**](enable-allocate.md) | Especifica que o código de stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 