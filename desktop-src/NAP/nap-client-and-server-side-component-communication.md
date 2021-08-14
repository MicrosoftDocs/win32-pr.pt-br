---
title: Comunicação de cliente NAP e componente do lado do servidor
description: Comunicação de cliente NAP e componente do lado do servidor
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3c390aa8bdc8cc80eec8834dd1c250d523737d63963b4b9370877ffa46329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799063"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicação de cliente NAP e componente do lado do servidor

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O componente agente NAP pode se comunicar com o componente servidor de administração NAP por meio do seguinte processo:

1.  O Agente NAP passa o SSoH para o NAP EC.
2.  O NAP EC passa o SSoH para o NAP ES.
3.  O NAP ES passa o SSoH para o serviço NPS (Servidor de Políticas de Rede).
4.  O serviço NPS passa o SSoH para o Servidor de Administração NAP.

Um SHA pode se comunicar com seu SHV correspondente por meio do seguinte processo:

1.  O SHA passa seu SoH para o Agente NAP.
2.  O Agente NAP passa o SoH, contido no SSoH, para o NAP EC.
3.  O NAP EC passa o SoH para o NAP ES.
4.  O NAP ES passa o SoH para o Servidor de Administração NAP.
5.  O Servidor de Administração NAP passa o SoH para o SHV.

A figura a seguir mostra o processo de comunicação de componentes cliente NAP para componentes nap do lado do servidor.

![arquitetura de comunicação de cliente para servidor na plataforma nap](images/nap-client-to-server-comm.png)

O Servidor de Administração NAP pode se comunicar com o Agente NAP por meio do seguinte processo:

1.  O Servidor de Administração NAP passa os SoHRs para o serviço NPS.
2.  O serviço NPS passa o SSoHR para o NAP ES.
3.  O NAP ES passa o SSoHR para o NAP EC.
4.  O NAP EC passa o SSoHR para o Agente NAP.

O SHV pode se comunicar com seu SHA correspondente por meio do seguinte processo:

1.  O SHV passa seu SoHR para o Servidor de Administração NAP.
2.  O Servidor de Administração NAP passa o SoHR para o serviço NPS.
3.  O serviço NPS passa o SoHR, contido no SSoHR, para o NAP ES.
4.  O NAP ES passa o SoHR para o NAP EC.
5.  O NAP EC passa o SoHR para o Agente NAP.
6.  O Agente NAP passa o SoHR para o SHA.

A figura abaixo mostra o processo de comunicação de componentes do lado do servidor NAP para componentes cliente NAP.

![arquitetura de comunicação de servidor para cliente na plataforma nap](images/nap-server-to-client-comm.png)

 

 




