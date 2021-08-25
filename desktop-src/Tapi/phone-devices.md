---
description: Telefone suporte a dispositivos é suplementar em vez de básico, portanto, os provedores de serviços não são necessários para dar suporte a dispositivos de telefone.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Telefone Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d11aa269e17d74fbaf74c701c954ced734ef33900198a7c9e30a044f5ebd32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873276"
---
# <a name="phone-devices"></a>Telefone Dispositivos

Telefone suporte a dispositivos é suplementar em vez de básico, portanto, os provedores de serviços não são necessários para dar suporte a dispositivos de telefone.

Assim como uma classe de dispositivo de linha é uma abstração de um dispositivo de linha física, a classe de dispositivo de telefone representa uma abstração independente do dispositivo de um conjunto de telefones. A TAPI trata dispositivos de linha e telefone como dispositivos independentes uns dos outros. Em outras palavras, você pode usar um telefone (dispositivo) sem usar uma linha associada e pode usar uma linha (dispositivo) sem usar um telefone.

Provedores de serviços que implementam totalmente essa independência podem oferecer usos para esses dispositivos não definidos pelos protocolos de telefonia tradicionais. Por exemplo, uma pessoa pode usar o telefone da área de trabalho como um dispositivo de áudio de forma de onda para gravação ou reprodução de voz, talvez sem o conhecimento da opção de que o telefone está em uso. Nessa implementação, a elevação do telefone local não precisa enviar automaticamente um sinal de offhook para a opção.

Essa independência também permite que um aplicativo toque no telefone local de maneira independente das chamadas de entrada. Os recursos dos provedores de serviços são limitados pelos recursos de hardware e software usados para interconectar a opção, o telefone e o computador.

A TAPI inclui funções para recuperar recursos de dispositivo que permitem que os clientes determinem se há suporte para esse modelo de uso.

Esta seção descreve os dispositivos de telefone e explica como usar as funções de telefone TAPI para acessar esses dispositivos.

-   [Telefone Dispositivo](phone-device-elements.md)
-   [Inicialização e desligamento](initialization-and-shutdown.md)

 

 



