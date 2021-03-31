---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159824"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Texto

A variante retornada de {0} deve ser um {1} , mas é um {2} .

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento está relatando um estado de MSAA inválido. Por exemplo, o método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usado para recuperar o estado de MSAA de um elemento deve retornar um valor inteiro que representa uma das constantes de estado de MSAA, mas está retornando outra variante em vez disso.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um estado de elemento incorreto pode ser relatado ao usuário.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um estado de MSAA definido incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado do objeto**](object-state-constants.md)
</dt> </dl>

 

 




