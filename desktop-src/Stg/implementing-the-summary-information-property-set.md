---
title: Implementando o conjunto de propriedades de informações de resumo
description: Há diretrizes a seguir ao implementar um conjunto de propriedades de informações resumidas para Armazenamento.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementando o conjunto de propriedades de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe847d9a7353074727c94250d0f1ec1fec2194b5b7d250099464a86667861f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796906"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementando o conjunto de propriedades de informações de resumo

Há diretrizes a seguir ao implementar um conjunto de propriedades de informações resumidas para Armazenamento.

Veja a seguir as diretrizes para implementar o [Conjunto de Propriedades de Informações resumidas](the-summary-information-property-set.md):

-   **PID \_ TEMPLATE** refere-se a um documento externo que contém informações de formato e estilo. O processo pelo qual o modelo está localizado é definido pela implementação.
-   **PID \_ LASTAUTHOR** é o nome armazenado em Informações do Usuário pelo aplicativo. Por exemplo, Maria cria um documento em seu computador e o fornece a João, que o modifica e salva. Maria é a autora, João é o último salvo por valor.
-   **PID \_ REVNUMBER** é o número de vezes que o comando Arquivo/Salvar foi chamado neste documento.
-   Cada um dos valores de data/hora deve ser armazenado em UTC (Tempo Coordenado Universal).
-   **PID \_ CREATE \_ DTM** é uma propriedade somente leitura; essa propriedade deve ser definida quando um documento é criado, mas não deve ser alterado posteriormente.
-   Para **a MINIATURA \_ PID, os** aplicativos devem armazenar dados no formato CF **\_ DIB** ou **CF \_ METAFILEPICT.** **CF \_ METAFILEPICT** é recomendado.
-   **PID \_ SECURITY** é o nível de segurança sugerido para o documento. Ao notar o nível de segurança no documento, um aplicativo diferente do originador do documento pode ajustar sua interface do usuário às propriedades. Um aplicativo não deve exibir informações sobre um documento protegido por senha ou habilitar modificações em documentos Read-Only ou Bloqueado para Anotações. Se o usuário tentar modificar as propriedades, o aplicativo deverá avisar o usuário sobre o status Read-Only Recomendado.



| Nível de segurança         | Valor |
|------------------------|-------|
| Nenhum                   | 0     |
| Senha protegida     | 1     |
| Recomendado somente leitura  | 2     |
| Imposto somente leitura     | 4     |
| Bloqueado para anotações | 8     |



 

 

 




