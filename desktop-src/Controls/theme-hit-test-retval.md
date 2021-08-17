---
title: Valores de retorno de teste de clique
description: Esta seção lista os valores de código de teste de clique que são retornados no parâmetro pwHitTestCode da função HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020765e6f766efc2c79e869a1b06cfceac2c13a451cc381d88ae066cc1478c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797596"
---
# <a name="hit-test-return-values"></a>Valores de retorno de teste de clique

Esta seção lista os valores de código de teste de clique que são retornados no parâmetro *pwHitTestCode* da função [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Os valores de código retornados dependem das opções de teste de clique especificadas no parâmetro *dwOptions* da função **HitTestThemeBackground** . Para obter uma lista das opções, consulte [Opções de teste de clique](theme-hit-test-options.md).

## <a name="return-values"></a>Valores de retorno

A tabela a seguir lista as opções de teste de clique e os códigos de retorno correspondentes.



| Opção                       | Códigos de retorno  | Descrição                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | Teste de clique bem-sucedido no segmento de borda inferior.                                                                   |
|                              | HTBOTTOMLEFT  | Teste de clique bem-sucedido na interseção da borda inferior e esquerda.                                                     |
|                              | HTBOTTOMRIGHT | Teste de clique bem-sucedido na interseção de borda inferior e direita.                                                    |
|                              | HTCLIENT      | Teste de clique bem-sucedido no segmento do segundo plano.                                                               |
|                              | HTLEFT        | Teste de clique bem-sucedido no segmento de borda à esquerda.                                                                     |
|                              | HTNOWHERE     | O teste de clique foi bem-sucedido fora do controle ou em uma área transparente.                                                   |
|                              | HTRIGHT       | Teste de clique bem-sucedido no segmento de borda direita.                                                                    |
|                              | HTTOP         | Teste de clique bem-sucedido no segmento de borda superior.                                                                      |
|                              | HTTOPLEFT     | Teste de clique bem-sucedido na interseção da borda superior e esquerda.                                                            |
|                              | HTTOPRIGHT    | Teste de clique bem-sucedido na interseção da borda superior e direita.                                                       |
| \_legenda HTTB                | HTCAPTION     | Teste de clique bem-sucedido nos segmentos de segundo plano superior, superior esquerdo ou superior direito.                                         |
|                              | HTNOWHERE     | O teste de clique foi bem-sucedido fora do controle ou em uma área transparente.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | Teste de clique bem-sucedido em qualquer segmento de segundo plano, exceto o segmento de segundo plano.                                 |
|                              | HTCLIENT      | Teste de clique bem-sucedido no segmento do segundo plano.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | Falha no teste de clique no segmento do segundo plano e nas zonas de redimensionamento, mas com êxito em um segmento de borda de segundo plano. |
| HTTB \_ RESIZINGBORDER \_ inferior | HTBOTTOM      | Teste de clique bem-sucedido no segmento de borda inferior.                                                                   |
| HTTB \_ RESIZINGBORDER \_ Left   | HTLEFT        | Teste de clique bem-sucedido no segmento de borda à esquerda.                                                                     |
| HTTB \_ RESIZINGBORDER \_ Right  | HTRIGHT       | Teste de clique bem-sucedido no segmento de borda direita.                                                                    |
| HTTB \_ RESIZINGBORDER \_ superior    | HTTOP         | Teste de clique bem-sucedido no segmento de borda superior.                                                                      |



 

 

 




