---
description: O WIA é implementado como um servidor de Component Object Model (COM) fora do processo para garantir a operação robusta de aplicativos cliente.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Arquitetura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549927"
---
# <a name="wia-architecture"></a>Arquitetura WIA

O WIA é implementado como um servidor de Component Object Model (COM) fora do processo para garantir a operação robusta de aplicativos cliente. Ao contrário da maioria dos aplicativos de servidor de processo, a WIA (aquisição de imagem do Windows) evita penalidades de desempenho durante a transferência de dados de imagem, fornecendo seu próprio mecanismo de transferência de dados, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer). Essa interface de alto desempenho usa uma janela de memória compartilhada para transferir dados para o cliente.

O WIA tem três componentes principais: um Gerenciador de Dispositivos, uma biblioteca de serviços minidriver e um dispositivo minidriver.

-   O Gerenciador de Dispositivos enumera dispositivos de geração de imagens, recupera propriedades de dispositivo, configura eventos para dispositivos e cria objetos de dispositivo.
-   A biblioteca de serviço minidriver implementa todos os serviços que são independentes de dispositivo.
-   O dispositivo minidriver mapeia Propriedades e comandos WIA para o dispositivo específico.

O diagrama a seguir ilustra a arquitetura WIA:

![arquitetura WIA](images/wiarch.gif)

 

 



