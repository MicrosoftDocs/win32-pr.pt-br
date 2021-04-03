---
title: Sinalizadores do próximo salto
description: Sinalizadores do próximo salto
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Avançar
- Sinalizadores do próximo salto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006004"
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



 

 

 




