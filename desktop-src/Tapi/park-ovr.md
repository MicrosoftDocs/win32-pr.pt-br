---
description: A operação de estacionamento permite que um aplicativo envie uma sessão para um endereço especial onde ele será mantido até que seja desestacionado.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Parque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779450"
---
# <a name="park"></a>Parque

A operação de estacionamento permite que um aplicativo envie uma sessão para um endereço especial onde ele será mantido até que seja desestacionado. Do ponto de vista do aplicativo, isso é muito parecido com uma transferência. Para a parte na outra extremidade da conexão, isso se parece ser colocado em espera.

A diferença entre o estacionamento e a transferência é que o endereço estacionado não é um ponto de conexão para a sessão, e a sessão não alerta ou atingiu o tempo limite. A diferença entre o estacionamento e o Hold é que, após a conclusão da operação de estacionamento, a sessão não estará mais associada ao endereço do aplicativo.

São fornecidas duas formas de estacionamento de uma sessão: *Parque direcionado* e *estacionamento não direcionado*. No parque de chamada direcionada, o aplicativo especifica o endereço de destino onde a chamada deve ser estacionada. Com o estacionamento não direcionado, o provedor de serviços ou o hardware subjacente determina o endereço e o retorna para o aplicativo.

Uma sessão estacionada normalmente entra no estado ocioso após ter sido estacionada com êxito e o aplicativo deve liberar os recursos associados a ele. Consulte [encerrar uma sessão](terminate-a-session-ovr.md) para obter um resumo de como fazer isso.

Se o aplicativo desestacionar a sessão, novos recursos de sessão serão alocados mesmo que o aplicativo tenha retornado os ponteiros anteriores, de modo que a falha de fazer as versões corretas pode resultar em uma variedade de problemas.

Alguns provedores de serviços podem lembrar o usuário após uma sessão ter sido estacionada por um longo período de tempo. O aplicativo vê uma chamada de oferta com um [motivo](reason-ovr.md) de chamada definido como lembrete.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Consulte [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
