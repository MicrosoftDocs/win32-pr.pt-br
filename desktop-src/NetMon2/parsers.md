---
description: Um analisador é o componente Monitor de Rede que inspeciona dados em uma captura atrasada e passa informações de protocolo específicas para o aplicativo que chama o analisador. Um analisador é passivo porque funciona somente quando Monitor de Rede ou um especialista o chama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826825"
---
# <a name="parser"></a>Analisador

Um analisador é o componente Monitor de Rede que inspeciona dados em uma [*captura atrasada*](d.md)e passa informações de protocolo específicas para o aplicativo que chama o analisador. Um analisador é passivo porque funciona somente quando Monitor de Rede ou um [*especialista*](e.md) o chama.

Cada analisador identifica um protocolo e, normalmente, um analisador é implementado em sua própria DLL do analisador. No entanto, uma DLL do analisador pode conter vários analisadores, o que significa que uma DLL pode ser usada para detectar mais de um protocolo.

Os dados passados para um analisador são tirados de uma [*captura atrasada*](d.md)e passados para o analisador em uma base quadro a quadro. Você não pode analisar uma captura em tempo real.

Para analisar os dados em um quadro, o analisador deve reconhecer a instância de protocolo, identificar as propriedades que existem na instância de protocolo e anexar uma definição de propriedade a cada propriedade. Lembre-se de que o quadro contém apenas um fluxo de dados. O quadro não contém dados que indicam quais protocolos ou propriedades de protocolo os dados representam.

A ilustração a seguir mostra um quadro que contém uma instância de um protocolo.

![um quadro que contém uma instância de protocolo](images/parser1.png)

Se Monitor de Rede for exibir dados analisados na interface do usuário, o analisador deverá formatar os dados. No entanto, alguns especialistas usam a saída do analisador programaticamente e não exibem a saída na interface do usuário do Monitor de Rede. Os dados exibidos incluem dados definidos pelo analisador e os dados na captura. Por exemplo, o analisador normalmente fornece um nome para uma propriedade que é exibida e os dados na captura que está associado à propriedade.



| Para obter informações sobre                                         | Consulte                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Quais pontos de entrada devem ser implementados dentro da DLL do analisador. | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                 |
| Como implementar funções de exportação de DLL do parser.                 | [Gravando um analisador de protocolo](writing-a-protocol-parser.md)             |
| Quais analisadores de funções e estruturas usam.                   | [Funções e estruturas do analisador](parser-functions-and-structures.md) |



 

 

 



