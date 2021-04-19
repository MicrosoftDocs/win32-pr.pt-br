---
description: '\_Constantes personalizadas de localidade \*'
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: Constantes LOCALE_CUSTOM *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778574"
---
# <a name="locale_custom-constants"></a>\_Constantes personalizadas de localidade \*

Este tópico define as \_ constantes personalizadas de localidade \* usadas pelo NLS para representar as [localidades personalizadas](custom-locales.md).



| Valor                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_padrão personalizado de localidade \_     | **Windows Vista e posterior:** A localidade personalizada padrão. Quando uma função NLS deve retornar um identificador de localidade para uma [localidade suplementar](custom-locales.md) para o usuário atual, a função retorna esse valor em vez do [padrão de \_ usuário \_ de localidade](locale-user-default.md). O valor do \_ padrão personalizado de localidade \_ é 0x0C00.                                                                                                                                                                  |
| \_ \_ padrão da interface do usuário personalizada de localidade \_ | **Windows Vista e posterior:** A localidade personalizada padrão para o MUI. Os idiomas preferenciais da interface do usuário e os idiomas de interface do usuário preferenciais do sistema podem incluir, no máximo, uma única linguagem implementada por um LIP (Language Interface Pack) e para o qual o identificador de idioma corresponde a uma localidade complementar. Se houver tal linguagem em uma lista, a constante será usada para fazer referência a esse idioma em determinados contextos. O valor do \_ padrão da interface do usuário personalizada de localidade \_ \_ é 0x1400.                    |
| LOCALIDADE \_ personalizada \_ não especificada | **Windows Vista e posterior:** Uma localidade personalizada não especificada, usada para identificar todas as localidades complementares, exceto a localidade do usuário atual. As localidades complementares não podem ser diferenciadas umas das outras por seus identificadores de localidade, mas podem ser diferenciadas por seus [nomes de localidade](locale-names.md). Algumas funções NLS podem retornar essa constante para indicar que elas não podem fornecer um identificador útil para uma localidade específica. O valor de local \_ personalizado não \_ especificado é 0x1000. |



 

 

 



