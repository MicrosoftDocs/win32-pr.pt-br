---
description: Um provedor de tempo é implementado como uma DLL. Cada DLL pode dar suporte a vários provedores de tempo. Cada provedor é responsável por sua própria configuração e sincronização.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Criando um provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58766bf0ed7339bf8c9bfd7abc7434ddc43165b7cbdd77bcfd5420947e743d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885759"
---
# <a name="creating-a-time-provider"></a>Criando um provedor de tempo

Um provedor de tempo é implementado como uma DLL. Cada DLL pode dar suporte a vários provedores de tempo. Cada provedor é responsável por sua própria configuração e sincronização.

Os provedores de tempo devem implementar as seguintes funções de retorno de chamada:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Depois de carregar a DLL do provedor, o Gerenciador de provedores de tempo chama [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passando o nome do provedor e os ponteiros para as seguintes funções:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Essas funções são para uso pelo provedor de tempo. O provedor de tempo usa [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) para retornar um identificador de provedor que o Gerenciador de provedores de tempo usa ao enviar comandos para o provedor de tempo. O valor do identificador é definido pelo provedor de tempo e é usado principalmente para distinguir entre diferentes provedores implementados na mesma DLL. O provedor de tempo pode registrar eventos significativos usando [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

O Gerenciador de provedores de tempo usa [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) para enviar comandos para o provedor de tempo. Quando o provedor de tempo precisa notificar o Gerenciador de provedores de tempo de que ele tem exemplos de tempo disponíveis, ele chama [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). Em seguida, o Gerenciador de provedores de tempo chama **TimeProvCommand** com o \_ comando TPC getsamples para recuperar os exemplos de tempo. Pode levar até 16 segundos para que o Gerenciador do provedor de tempo solicite o exemplo. Portanto, o aplicativo não deve aguardar a solicitação.

Para garantir a exatidão, o provedor de tempo deve recuperar todas as informações relacionadas ao tempo usando [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Quando é hora de desligar o provedor de tempo, o Gerenciador de provedores de tempo chama [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



