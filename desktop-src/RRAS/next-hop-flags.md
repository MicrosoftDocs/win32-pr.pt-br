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
| Estado de NEXTHOP do RTM \_ \_ \_ criado | 0     | Indica que o próximo salto foi criado. |
| Estado de NEXTHOP do RTM \_ \_ \_ excluído | 1     | Indica que o próximo salto foi excluído. |



 

## <a name="next-hop-flags"></a>Sinalizadores do próximo salto



| Constante                    | Valor  | Descrição                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| sinalizadores de NEXTHOP do RTM \_ \_ \_ remotos | 0x0001 | Este próximo salto aponta para um destino remoto que não está acessível diretamente. Para obter o caminho completo, o cliente deve executar uma pesquisa recursiva. |
| sinalizadores de NEXTHOP do RTM \_ \_ \_ inativos   | 0x0002 | Esse sinalizador é reservado para uso futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Próximo salto adicionado



| Constante                  | Valor | Descrição                 |
|---------------------------|-------|-----------------------------|
| \_ \_ nova alteração de NEXTHOP do RTM \_ | 0x01  | Um novo salto seguinte foi criado. |



 

 

 




