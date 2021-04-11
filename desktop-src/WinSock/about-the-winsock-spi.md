---
description: O Winsock fornece uma interface de provedor de serviços para a criação de serviços de Winsock, comumente chamados de SPI do Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Sobre o SPI do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090412"
---
# <a name="about-the-winsock-spi"></a>Sobre o SPI do Winsock

O Winsock fornece uma interface de provedor de serviços para a criação de serviços de Winsock, comumente chamados de SPI do Winsock. Existem dois tipos de provedores de serviços: provedores de transporte e provedores de namespace. Exemplos de provedores de transporte incluem pilhas de protocolo, como TCP/IP ou IPX/SPX, enquanto um exemplo de um provedor de namespace seria uma interface para o DNS (sistema de cadastramento de domínio) da Internet. Seções separadas da especificação da interface do provedor de serviços se aplicam a cada tipo de provedor de serviços.

Os provedores de serviço de [namespace](name-space-service-providers-2.md) e [transporte](transport-service-providers-2.md) devem ser registrados com o \_32.dll Ws2 no momento em que são instalados. Esse registro só precisa ser feito uma vez para cada provedor, pois as informações necessárias são mantidas no armazenamento persistente.

 

 



