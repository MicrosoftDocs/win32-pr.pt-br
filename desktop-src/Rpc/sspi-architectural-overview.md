---
title: Visão geral da arquitetura SSPI
description: O SSPI é uma interface de software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007894"
---
# <a name="sspi-architectural-overview"></a>Visão geral da arquitetura SSPI

O SSPI é uma interface de software. Bibliotecas de programação distribuídas, como RPC, podem usá-las para comunicações autenticadas. Um ou mais módulos de software fornecem os recursos de autenticação reais. Cada módulo, chamado de SSP (provedor de suporte de segurança), é implementado como uma DLL (biblioteca de vínculo dinâmico). Um SSP fornece um ou mais pacotes de segurança.

Uma variedade de SSPs e pacotes estão disponíveis. O Windows é fornecido com o pacote de segurança do NTLM e o pacote de segurança do protocolo Microsoft Kerberos. Além disso, você pode optar por instalar o pacote de segurança SSL (Secure Socket Layer) ou qualquer outro SSP compatível com o SSPI.

O uso de SSPI garante que, independentemente do SSP que você selecionar, seu aplicativo acesse os recursos de autenticação de maneira uniforme. Esse recurso fornece ao seu aplicativo maior independência da implementação da rede do que estava disponível no passado.

Os aplicativos distribuídos se comunicam através da interface RPC. O software RPC, por sua vez, acessa os recursos de autenticação de um SSP por meio do SSPI.

Para obter mais informações, consulte [SSPI](/windows/desktop/SecAuthN/sspi).

 

 