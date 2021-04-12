---
title: Comunicação do cliente NAP e do componente do lado do servidor
description: Comunicação do cliente NAP e do componente do lado do servidor
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364348"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicação do cliente NAP e do componente do lado do servidor

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O componente agente NAP pode se comunicar com o componente de servidor de administração NAP por meio do seguinte processo:

1.  O agente NAP passa o SSoH para o NAP EC.
2.  O NAP EC passa o SSoH para o NAP ES.
3.  O NAP ES passa o SSoH para o serviço de servidor de diretivas de rede (NPS).
4.  O serviço NPS passa o SSoH para o servidor de administração NAP.

Um SHA pode se comunicar com seu SHV correspondente por meio do seguinte processo:

1.  O SHA passa seu SoH para o agente NAP.
2.  O agente NAP passa a SoH, contida no SSoH, para a NAP EC.
3.  O NAP EC passa a SoH para a NAP ES.
4.  O NAP ES passa a SoH para o servidor de administração de NAP.
5.  O servidor de administração NAP passa a SoH para o SHV.

A figura a seguir mostra o processo de comunicação de componentes de cliente NAP para componentes do lado do servidor NAP.

![arquitetura de cliente para comunicação de servidor na plataforma NAP](images/nap-client-to-server-comm.png)

O servidor de administração NAP pode se comunicar com o agente NAP por meio do seguinte processo:

1.  O servidor de administração NAP passa o SoHRs para o serviço NPS.
2.  O serviço NPS passa o SSoHR para o NAP ES.
3.  O NAP ES passa o SSoHR para o NAP EC.
4.  O NAP EC passa o SSoHR para o agente NAP.

O SHV pode se comunicar com seu SHA correspondente por meio do seguinte processo:

1.  O SHV passa seu SoHR para o servidor de administração de NAP.
2.  O servidor de administração NAP passa o SoHR para o serviço NPS.
3.  O serviço NPS passa o SoHR, contido dentro do SSoHR, para a NAP ES.
4.  O NAP ES passa o SoHR para o NAP EC.
5.  O NAP EC passa o SoHR para o agente NAP.
6.  O agente NAP passa o SoHR para o SHA.

A figura a seguir mostra o processo de comunicação de componentes do lado do servidor NAP para componentes de cliente NAP.

![arquitetura de servidor para comunicação de cliente na plataforma NAP](images/nap-server-to-client-comm.png)

 

 




