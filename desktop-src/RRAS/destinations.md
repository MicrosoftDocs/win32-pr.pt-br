---
title: Destinos
description: Um destino na tabela de roteamento é uma entrada de rede representada por um endereço de rede e uma máscara de rede.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822699"
---
# <a name="destinations"></a>Destinos

Um destino na tabela de roteamento é uma entrada de rede representada por um endereço de rede e uma máscara de rede.

Uma entrada de destino na tabela de roteamento inclui:

-   O endereço, expresso como um endereço de rede e uma máscara de rede.
-   Uma lista de rotas para o destino.
-   Uma lista de Slots de ponteiro opacos.
-   As exibições nas quais esse destino é válido. O destino contém uma estrutura para cada exibição que contém as seguintes informações:
    -   Um identificador para a exibição.
    -   Um ponteiro para a melhor rota para o destino nesta exibição.
    -   O proprietário da melhor rota nessa exibição.
    -   Sinalizadores associados à melhor rota nesta exibição.
    -   Identificador para qualquer rota que esteja em um estado suspenso nesta exibição.

 

 




