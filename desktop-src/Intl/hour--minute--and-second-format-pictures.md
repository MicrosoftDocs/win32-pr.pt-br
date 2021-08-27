---
description: Este tópico descreve os tipos de formato para cadeias de caracteres usadas para compor a imagem de formato para uma cadeia de tempo. Cada imagem de formato consiste em uma combinação de uma cadeia de caracteres de cada um dos tipos de formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Imagens de formato de hora, minuto e segundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e201e72e4da621334a46f20c47e1dd5f731d7ea443bb9970ce07bb7f4e5455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130386"
---
# <a name="hour-minute-and-second-format-pictures"></a>Imagens de formato de hora, minuto e segundo

Este tópico descreve os tipos de formato para cadeias de caracteres usadas para compor a imagem de formato para uma cadeia de tempo. Cada imagem de formato consiste em uma combinação de uma cadeia de caracteres de cada um dos tipos de formato.

> [!Note]  
> Nos tipos de formato, as letras "m", "s" e "t" devem estar em minúsculas e a letra "h" deve ser minúscula para indicar o relógio de 12 horas ou maiúsculas ("H") para denotar o relógio de 24 horas.

Aspas simples podem ser usadas para marcar caracteres que devem ser exibidos exatamente como especificado. Se o aplicativo precisar exibir uma aspa simples, ele deverá posicionar duas aspas simples em uma linha. Por exemplo, ' abc ' ' bar ', é exibido como "abc'bar".

A tabela a seguir define os tipos de formato usados para representar horas.

| String | Significado                                                             |
|--------|---------------------------------------------------------------------|
| h      | Horas sem zeros à esquerda para horas de dígito único (relógio de 12 horas). |
| hh     | Horas com zeros à esquerda para horas de dígito único (relógio de 12 horas).    |
| H      | Horas sem zeros à esquerda para horas de dígito único (relógio de 24 horas). |
| HH     | Horas com zeros à esquerda para horas de dígito único (relógio de 24 horas).    |

A tabela a seguir define os tipos de formato usados para representar minutos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| m      | Minutos sem zeros à esquerda para minutos de dígito único. |
| MM     | Minutos com zeros à esquerda para minutos de dígito único.    |

A tabela a seguir define os tipos de formato usados para representar segundos.

| String | Significado                                                 |
|--------|---------------------------------------------------------|
| s      | Segundos sem zeros à esquerda para segundos de dígito único. |
| ss     | Segundos com zeros à esquerda para segundos de dígito único.    |

A tabela a seguir define os tipos de formato usados para representar um marcador de tempo.

| String | Significado|
| ---    | ---    |
| t      | Cadeia de caracteres do marcador de tempo de um caractere.<br />**Observação:** Esse formato não é recomendado para uso com determinados idiomas, como japonês (Japão). Com esse formato, um aplicativo sempre usa o primeiro caractere da cadeia de caracteres do marcador de tempo, definido por [LOCALE_S1159](locale-s1159.md) (AM) e [LOCALE_S2359](locale-s2359.md) (PM). Por isso, o aplicativo pode criar formatação incorreta com a mesma cadeia de caracteres usada para AM e PM.|
| tt     | Cadeia de caracteres do marcador de tempo de vários caracteres. |
