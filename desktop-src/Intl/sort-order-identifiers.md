---
description: Este tópico descreve os identificadores de ordem de classificação, que podem ser usados na preparação de identificadores de localidade.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Identificadores de ordem de classificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297606"
---
# <a name="sort-order-identifiers"></a>Identificadores de ordem de classificação

Este tópico descreve os identificadores de ordem de classificação, que podem ser usados na preparação de [identificadores de localidade](locale-identifiers.md). Um identificador de ordem de classificação é definido no formato " \_ SortOrder", no final do nome de localidade usado no identificador, por exemplo, "de-de \_ phoneb", em que "phoneb" é a ordem de classificação. O identificador de localidade correspondente é criado da seguinte maneira: `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Constante                      | Nome da localidade                                                                                         | Significado                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CLASSIFICAR \_ Big5 do chinês \_           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Ordem de BIG5 do chinês                                                |
| CLASSIFICAR \_ chinês \_ bopomofo       | zh-TW \_ pronun                                                                                       | Ordem do chinês tradicional bopomofo                                |
| CLASSIFICAR \_ o \_ catálogo telefônico em chinês \_    | ZH-CN \_ phoneb<br/>                                                                            | Ordem do catálogo telefônico chinês (sobrenome)                                |
| CLASSIFICAR em \_ chinês \_ PRC            | zh – traço do CN \_<br/> zh – \_ traço HK<br/> zh – \_ traço mo<br/> zh – \_ traço SG<br/> | Ordem de contagem de traços da PRC do China                                    |
| CLASSIFICAR \_ PRCP em chinês \_           | zh-CN<br/> zh-SG<br/>                                                                   | Ordem fonética do PRC chinês                                        |
| CLASSIFICAR \_ RADICALSTROKE em chinês \_  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Radical do chinês/ordem do traço                                      |
| CLASSIFICAR \_ Unicode em chinês \_        | —                                                                                                   | Ordem Unicode do chinês **Windows 2000:** sem suporte.<br/>  |
| CLASSIFICAR \_ padrão                 | Nome da localidade que é igual ao nome do idioma correspondente                                     | Ordem de classificação padrão                                                |
| CLASSIFICAR \_ georgiano \_ moderno        | Ka-GE \_ moderno                                                                                       | Ordem moderna georgiano                                             |
| CLASSIFICAR \_ georgiano \_ tradicional   | ka-GE                                                                                               | Ordem tradicional georgiano                                        |
| CLASSIFICAR \_ o \_ catálogo telefônico alemão \_     | phoneb de remoção \_                                                                                       | Ordem do catálogo telefônico alemão                                           |
| CLASSIFICAR \_ \_ padrão húngaro      | hu-HU                                                                                               | Ordem padrão de húngaro                                           |
| CLASSIFICAR \_ \_ técnico húngaro    | hu-HU \_ technl                                                                                       | Pedido técnico húngaro                                         |
| CLASSIFICAR \_ RADICALSTROKE japonesas \_ | ja-JP                                                                                               | Radical/traço Japonês ordem                                     |
| CLASSIFICAR \_ Unicode em Japonês \_       | —                                                                                                   | Ordem Unicode japonesa **Windows 2000:** sem suporte.<br/> |
| CLASSIFICAR \_ XJIS japonesas \_          | ja-JP                                                                                               | Ordem XJIS japonesa                                               |
| CLASSIFICAR \_ \_ KS coreano             | ko-KR                                                                                               | Ordem KS em coreano                                                  |
| CLASSIFICAR \_ \_ Unicode coreano         | —                                                                                                   | Ordem Unicode coreana **Windows 2000:** sem suporte.<br/>   |



 

 

 




