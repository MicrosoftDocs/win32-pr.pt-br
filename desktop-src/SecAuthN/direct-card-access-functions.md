---
description: Usando o subsistema de cartão inteligente, você pode se comunicar com cartões que podem não estar em conformidade com as especificações iso 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funções de acesso de cartão direto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72b606cd766ea9a8930599bd2a44e117dea0bffdef6474c038b39294c08acf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008454"
---
# <a name="direct-card-access-functions"></a>Funções de acesso de cartão direto

Usando o [*subsistema de cartão*](/windows/desktop/SecGloss/s-gly) inteligente, você pode se comunicar com cartões que podem não estar em conformidade com as especificações iso 7816. Para fazer isso, as funções a seguir permitem controlar os atributos das comunicações entre o aplicativo e o cartão, dando a você manipulação direta e de baixo nível do [*leitor.*](/windows/desktop/SecGloss/r-gly)

Para usar essas funções, você precisa fornecer um identificador para o atributo em questão. Para valores e identificadores de atributo válidos, consulte a Tabela 3-1 em *Requisitos para dispositivos PC-Connected interface .*



| Tópico                                    | Descrição                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Forneça controle direto do leitor. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obter atributos de leitor.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Definir atributo de leitor.                 |



 

 

 
