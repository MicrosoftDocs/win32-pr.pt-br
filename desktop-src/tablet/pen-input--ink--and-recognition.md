---
description: Um novo recurso interessante do Tablet PC é o sistema de entrada de caneta.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada, tinta e reconhecimento de caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8645a1a68499975ad3ef5cdafb8c07685e9ed9e600cdc9ca2129babaa8b953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716255"
---
# <a name="pen-input-ink-and-recognition"></a>Entrada, tinta e reconhecimento de caneta

Um novo recurso interessante do Tablet PC é o sistema de entrada de caneta. Todos os computadores do Tablet PC têm um digitalizador sob a tela que aceita entrada à caneta. Esse novo mecanismo de entrada exige que você pense em como criar aplicativos especificamente para Tablet PC. A API (interface de programação de aplicativo) da plataforma do Tablet PC ajuda você a fazer isso.

## <a name="collection-data-management-and-recognition"></a>Coleta, Gerenciamento de Dados e reconhecimento

A plataforma do Tablet PC pode ser dividida em três áreas distintas:

-   Coleção de tinta (objetos que são usados para coletar tinta do digitalizador).
-   Gerenciamento de dados de tinta (objetos que são usados para gerenciar a tinta coletada).
-   Reconhecimento de tinta (objetos que são usados para converter a tinta coletada em outros tipos de dados, como texto).

A imagem a seguir mostra, em um alto nível, como a API de coleta de tinta (API de caneta), a API de Gerenciamento de Dados de tinta (API de tinta) e a API de reconhecimento de tinta (API de reconhecimento) funcionam juntas na plataforma do Tablet PC.

![ilustração mostrando como a API de caneta, a API de tinta e a API de reconhecimento funcionam juntas](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

A API da plataforma do Tablet PC está disponível em APIs gerenciadas, bem como em uma biblioteca COM. Os tópicos a seguir descrevem os objetos na API e ilustram como os aplicativos usam esses objetos:

-   [Coleta de tinta](ink-collection.md)
-   [Dados de tinta](ink-data.md)
-   [Reconhecimento de tinta](ink-recognition.md)
-   [Análise de tinta](ink-analysis.md)
-   [reconhecimento de manuscrito no Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



