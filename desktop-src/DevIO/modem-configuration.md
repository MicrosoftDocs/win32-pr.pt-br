---
description: As funções de configuração de modem permitem configurar um modem antes de estabelecer uma conexão.
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: Configuração do modem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826568"
---
# <a name="modem-configuration"></a>Configuração do modem

As funções de configuração de modem permitem configurar um modem antes de estabelecer uma conexão. Um aplicativo pode definir opções de modem e determinar os recursos de um modem sem usar comandos específicos para qualquer dispositivo de modem. A seguir estão os recursos gerais que um aplicativo pode definir antes de fazer uma chamada:

-   Modo de operação primário (síncrono, assíncrono e se o controle de erro está habilitado).
-   Controle de erro V. 42 (definido pela CCITT recomendação V. 42), incluindo parâmetros específicos. CCITT significa o Telegraph internacional e o Comitê de consultoria por telefone.
-   V. 42bis (definido pela CCITT recomendação V. 42bis) e a compactação de dados MNP5.
-   Opções de tempo limite, incluindo configuração de chamada, inatividade e entrega de dados em buffer.

Antes de definir a configuração de um modem, um aplicativo deve determinar os recursos do dispositivo de modem usando a função [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) . Essa função preenche uma estrutura [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) . Essa estrutura contém uma parte geral, que se aplica a todos os dispositivos de comunicação e uma parte específica para cada subtipo de provedor. Para dispositivos de modem, a parte específica do provedor da estrutura **COMMPROP** é uma estrutura [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) .

Um aplicativo pode obter e definir a configuração atual de um modem usando as funções [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) , que usam uma estrutura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) . Essa estrutura contém uma parte geral, que se aplica a todos os dispositivos de comunicação e uma parte específica para cada subtipo de provedor. Para dispositivos de modem, a parte específica do provedor da estrutura **COMMCONFIG** é uma estrutura [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) .

Depois de configurar um modem, um aplicativo pode usar a TAPI (interface de programação de aplicativo de telefonia) para realmente estabelecer uma conexão.

As funções de configuração do modem não fornecem gerenciamento de longo prazo e manutenção de um modem. Os provedores de serviço de modem devem fornecer caixas de diálogo de configuração de modem para essa finalidade.

 

 



