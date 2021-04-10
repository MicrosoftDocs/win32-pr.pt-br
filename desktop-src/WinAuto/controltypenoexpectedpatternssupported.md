---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292249"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Texto

O elemento com um ControlType de {0} deve dar suporte a pelo menos um destes padrões: {1} mas esse elemento não

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O suporte à automação da interface do usuário do elemento não está em conformidade com a especificação de automação da interface do usuário porque o elemento deve dar suporte a pelo menos uma das listas de padrões de controle fornecidas, mas não. Como resultado, esse elemento pode não ser exposto corretamente a tecnologias assistenciais, o que pode ter um impacto sério na experiência do usuário.

## <a name="possible-causes"></a>Possíveis causas

-   Implementação de automação de interface do usuário incompleta.
-   A propriedade ControlType não está definida corretamente.

## <a name="remarks"></a>Comentários

AccChecker registra essa mensagem de erro para uma barra de progresso indeterminada. Você pode ignorar essa mensagem e/ou adicioná-la à lista de supressões.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




