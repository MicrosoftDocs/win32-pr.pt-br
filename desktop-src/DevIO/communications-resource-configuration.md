---
description: A estrutura COMMCONFIG define a configuração de um recurso de comunicação, serial ou de outra forma.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuração de recursos de comunicações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01cd85a60eabc3cf6adcbdb0e05d2fbdc662442029044a5ac67d9a37bc073d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918316"
---
# <a name="communications-resource-configuration"></a>Configuração de recursos de comunicações

A [**estrutura COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define a configuração de um recurso de comunicação, serial ou de outra forma. O formato da estrutura varia dependendo do tipo de recurso de comunicação (o subtipo do provedor). Os primeiros membros da estrutura são comuns a todos os recursos de comunicação; membros adicionais são definidos para subtipos de provedor específicos. Provedores de serviços específicos também podem estender a **estrutura COMMCONFIG.**

Um aplicativo pode obter e definir a configuração de um recurso de comunicação usando as funções [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) Quando aberto, um recurso de comunicação é inicializado usando a configuração padrão para seu subtipo de provedor. Para obter e definir a configuração padrão para um subtipo de provedor, use as funções [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) e [**SetDefaultCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)

Para solicitar informações de configuração ao usuário, use a [**função CommConfigDialog.**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) Essa função exibe uma caixa de diálogo definida pelo provedor de serviços e preenche uma [**estrutura COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) com base na entrada do usuário.

 

 



