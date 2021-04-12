---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364185"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Texto

Ao navegar chamando {0} a partir do nó testado e, em seguida, chamando repetidamente {1} , terminamos no seguinte filho: {2} . Isso não correspondeu ao resultado da chamada {3} no nó testado, que gerou: {4} . Em vez disso, o filho deve relatar como seu pai o nó de teste.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Há um problema ao navegar entre os filhos do elemento. 1. Uma implementação de automação de interface do usuário incorreta ou inválida.

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de automação de interface do usuário incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




