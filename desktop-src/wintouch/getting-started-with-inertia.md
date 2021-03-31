---
title: Inércia
description: Esta seção explica o inércia para o Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inércia
- inércia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005003"
---
# <a name="inertia"></a>Inércia

Esta seção explica o inércia para o Windows Touch.

A API do inércia incluída no Windows 7 permite o comportamento de objeto consistente em aplicativos do Windows Touch, fornecendo um modelo de física simples. O inércia é habilitado usando o processador inércia, uma classe que encapsula a funcionalidade. O processador inércia funciona processando eventos que são passados para ele quando as manipulações de objeto são concluídas e manipulando as trajetórias de objeto de forma consistente com outros aplicativos. Observe que o processador inércia está rigidamente acoplado ao processador de manipulação para simplificar a adição de suporte do inércia a aplicativos que usam manipulações. Na verdade, o processador inércia gera os mesmos eventos que o processador de manipulação faz. A seção a seguir explica como começar a usar o inércia.



| Seção                                                                      | Descrição                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Mecânica inércia](inertia-mechanics.md)                                   | Explica os fundamentos dos cálculos de inércia.                                                                             |
| [Manipulando inércia em código não gerenciado](handling-inertia-in-unmanaged-code.md) | Explica como usar a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para manipular o inércia em código não gerenciado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações e inércia](manipulation-and-inertia.md)
</dt> </dl>

 

 




