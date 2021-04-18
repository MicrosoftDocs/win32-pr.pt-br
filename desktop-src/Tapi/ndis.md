---
description: A classe de dispositivo NDIS consiste em dispositivos que podem ser associados a drivers de controle de acesso à mídia (NDIS) de especificação de interface de driver de rede para dar suporte a comunicações de rede. Você acessa esses dispositivos usando o functions.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: recepção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754186"
---
# <a name="ndis"></a>recepção

A classe de dispositivo NDIS consiste em dispositivos que podem ser associados a drivers de controle de acesso à mídia (NDIS) de especificação de interface de driver de rede para dar suporte a comunicações de rede. Você acessa esses dispositivos usando o functions.

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esses membros adicionais:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

O membro **hDevice** é o identificador a ser passado para um Mac, como o Mac assíncrono para rede dial-up, para associar uma conexão de rede com a conexão de chamada/modem. O membro **szDeviceType** é uma cadeia de caracteres terminada em nulo que especifica o nome do dispositivo associado ao identificador.

 

 



