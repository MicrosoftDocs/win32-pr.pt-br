---
description: A estrutura COMMCONFIG define a configuração de um recurso de comunicação, serial ou de outra forma.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuração de recursos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089205"
---
# <a name="communications-resource-configuration"></a>Configuração de recursos de comunicação

A estrutura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define a configuração de um recurso de comunicação, serial ou de outra forma. O formato da estrutura varia dependendo do tipo de recurso de comunicação (o subtipo do provedor). Os primeiros membros da estrutura são comuns a todos os recursos de comunicação; membros adicionais são definidos para subtipos de provedor específicos. Provedores de serviço específicos também podem estender a estrutura **COMMCONFIG** .

Um aplicativo pode obter e definir a configuração de um recurso de comunicação usando as funções [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . Quando aberto, um recurso de comunicação é inicializado usando a configuração padrão para seu subtipo de provedor. Para obter e definir a configuração padrão para um subtipo de provedor, use as funções [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) e [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Para solicitar informações de configuração ao usuário, use a função [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Essa função exibe uma caixa de diálogo definida pelo provedor de serviços e preenche uma estrutura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) com base na entrada do usuário.

 

 



