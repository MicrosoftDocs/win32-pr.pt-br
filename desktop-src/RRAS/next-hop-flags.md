---
title: Sinalizadores do próximo salto
description: Sinalizadores do próximo salto
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Avançar
- Sinalizadores do próximo salto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dbad78f5f10d7a9d7bf42f694f7e2fb3109c03b92dccdb5f31697f5cf8988c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790389"
---
# <a name="next-hop-flags"></a>Sinalizadores do próximo salto

## <a name="next-hop-state-flags"></a>Sinalizadores de estado do próximo salto



| Constante                     | Valor | Descrição                              |
|------------------------------|-------|------------------------------------------|
| RTM \_ NEXTHOP \_ STATE \_ CREATED | 0     | Indica que o próximo salto foi criado. |
| ESTADO \_ NEXTHOP \_ \_ RTM EXCLUÍDO | 1     | Indica que o próximo salto foi excluído. |



 

## <a name="next-hop-flags"></a>Sinalizadores do próximo salto



| Constante                    | Valor  | Descrição                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ NEXTHOP \_ FLAGS \_ REMOTE | 0x0001 | Este próximo salto aponta para um destino remoto que não está diretamente acessível. Para obter o caminho completo, o cliente deve executar uma análise recursiva. |
| RTM \_ NEXTHOP \_ SINALIZA PARA \_ BAIXO   | 0x0002 | Esse sinalizador é reservado para uso futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Próximo Salto Adicionado



| Constante                  | Valor | Descrição                 |
|---------------------------|-------|-----------------------------|
| RTM \_ NEXTHOP \_ CHANGE \_ NEW | 0x01  | Um novo próximo salto foi criado. |



 

 

 




