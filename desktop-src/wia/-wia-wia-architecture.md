---
description: O WIA é implementado como um servidor fora do processo Component Object Model (COM) para garantir a operação robusta de aplicativos cliente.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Arquitetura do WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a6bb88fba5a79f2915500786bbfcf8d531bfe0170ec6c6841f419425ee296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813256"
---
# <a name="wia-architecture"></a>Arquitetura do WIA

O WIA é implementado como um servidor fora do processo Component Object Model (COM) para garantir a operação robusta de aplicativos cliente. Ao contrário da maioria dos aplicativos de servidor fora do processo, o WIA (Aquisição de Imagem) do Windows evita penalidades de desempenho durante a transferência de dados de imagem, fornecendo seu próprio mecanismo de transferência de dados, [**IWiaDataTransfer.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) Essa interface de alto desempenho usa uma janela de memória compartilhada para transferir dados para o cliente.

O WIA tem três componentes principais: um Gerenciador de Dispositivos, uma Biblioteca de Serviços do Minidriver e um Minidriver de Dispositivo.

-   O Gerenciador de Dispositivos enumera dispositivos de imagens, recupera propriedades do dispositivo, configura eventos para dispositivos e cria objetos de dispositivo.
-   A Biblioteca de Serviços do Minidriver implementa todos os serviços que são independentes de dispositivo.
-   O Minidriver de Dispositivo mapeia propriedades e comandos wia para o dispositivo específico.

O diagrama a seguir ilustra a arquitetura do WIA:

![arquitetura wia](images/wiarch.gif)

 

 



