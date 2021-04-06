---
description: Usando o subsistema de cartão inteligente, você pode se comunicar com cartões que podem não estar em conformidade com as especificações ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funções de acesso de cartão direto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826822"
---
# <a name="direct-card-access-functions"></a>Funções de acesso de cartão direto

Usando o subsistema de [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) , você pode se comunicar com cartões que podem não estar em conformidade com as especificações ISO 7816. Para fazer isso, as funções a seguir permitem controlar os atributos das comunicações entre o aplicativo e o cartão fornecendo uma manipulação direta e de baixo nível do [*leitor*](/windows/desktop/SecGloss/r-gly).

Para usar essas funções, você precisa fornecer um identificador para o atributo em questão. Para obter os identificadores de atributo e valores válidos, consulte a tabela 3-1 em *requisitos para dispositivos de Interface PC-Connected*.



| Tópico                                    | Descrição                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Forneça controle direto do leitor. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obter atributos de leitor.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Definir atributo de leitor.                 |



 

 

 
