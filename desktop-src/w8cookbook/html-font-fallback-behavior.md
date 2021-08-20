---
title: Comportamento de fallback de fontes HTML
description: Comportamento de fallback de fontes HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eabc2c009657adc9b77775c550244c4bbe6a5a3b8b262c8ce915cab4f9e5756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672044"
---
# <a name="html-font-fallback-behavior"></a>Comportamento de fallback de fontes HTML

## <a name="platform"></a>Plataforma

Clientes-* * Windows 8.1  
**servidores-** Windows Server 2012 R2  


## <a name="description"></a>Descrição

a Microsoft está atualizando a lógica das fontes da interface do usuário para vários idiomas em aplicativos da Windows Store usando HTML. Em vez de usar uma única fonte para todos os idiomas, a fonte da interface do usuário agora será determinada de acordo com a linguagem. Por exemplo, as fontes de interface do usuário para japonês agora serão a interface do usuário do Meiryo em aplicativos que usam HTML.

## <a name="manifestation"></a>Manifestação

Os aplicativos que dependem de uma fonte antiga podem parecer diferentes; Embora a aparência do seu aplicativo seja aprimorada em geral graças a fontes mais legíveis, pode haver um problema com layouts que dependem de tamanhos de conteúdo de pixel perfeito. Por exemplo, algumas linhas de conteúdo podem ser maiores do que antes, causando quebras de linha inesperadas e/ou redimensionamento de elementos de contêiner. No entanto, na prática, não notamos nenhum problema com nenhum aplicativo existente.

## <a name="solution"></a>Solução

Os aplicativos afetados podem mitigar esse comportamento especificando uma determinada fonte por meio de CSS (por exemplo, "font-family: interface do usuário Meiryo") em vez de depender das fontes padrão antigas. A tabela a seguir fornece a fonte da interface do usuário para cada um dos nomes de script.



| Nome do script        | Fonte da interface do usuário               |
|--------------------|-----------------------|
| Árabe             | Interface do Usuário Segoe              |
| Armênia           | Interface do Usuário Segoe              |
| Bengali            | Nirmala UI            |
| Bopomofo           | Microsoft JhengHei UI |
| Braille            | Segoe UI Symbol       |
| Bugi           | Leelawadee UI         |
| Silábico canadense | Gadugi                |
| Cherokee           | Gadugi                |
| Copta             | Segoe UI Symbol       |
| Han (simplificado)   | Microsoft YaHei UI    |
| Han (tradicional)  | Microsoft JhengHei UI |
| Cirílico           | Interface do Usuário Segoe              |
| Devanagari         | Nirmala UI            |
| Deseret            | Segoe UI Symbol       |
| Etíope           | Ebrima                |
| Georgiano           | Interface do Usuário Segoe              |
| Letra         | Segoe UI Symbol       |
| Gothic             | Segoe UI Symbol       |
| Grego              | Interface do Usuário Segoe              |
| Guzerate           | Nirmala UI            |
| Gurmukhi           | Nirmala UI            |
| Hebraico             | Interface do Usuário Segoe              |
| Itálico antigo         | Segoe UI Symbol       |
| Javanês           | Texto do javanês         |
| Japonês           | Interface do usuário do amMeiryo             |
| canarim            | Interface do usuário do amMirmala            |
| Khmer              | Leelawadee UI         |
| Coreano             | Malgun Gothic         |
| Lao                | Leelawadee            |
| Latim              | Interface do Usuário Segoe              |
| Malaiala          | Nirmala UI            |
| Mongol          | Mongolian Baiti       |
| Myanmar            | Myanmar Text          |
| N' Ko               | Ebrima                |
| Ogham              | Segoe UI Symbol       |
| Ol Chiki           | Nirmala UI            |
| Turco antigo         | Segoe UI Symbol       |
| Oriya              | Nirmala UI            |
| Osmanya            | Ebrima                |
| Phags-Pa           | Microsoft PhagsPa     |
| Rúnica              | Segoe UI Symbol       |
| Sora Sompeng       | Nirmala UI            |
| Sinhala            | Nirmala UI            |
| Siríaco             | Estrangelo Erangelo     |
| Tai Le             | Microsoft Tai Le      |
| Tai Lue Novo        | Microsoft New Tai Lue |
| Tâmil              | Nirmala UI            |
| Télugo             | Nirmala UI            |
| Tifinagh           | Ebrima                |
| Thaana             | MV Boli               |
| Tailandês               | Leelawadee UI         |
| Tibetano            | Microsoft Himalaya    |
| Vai                | Ebrima                |
| Yi                 | Microsoft Yi Baiti    |



 

 

 




