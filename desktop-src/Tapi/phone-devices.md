---
description: O suporte a dispositivos telefônicos é suplementar em vez de básico, portanto, os provedores de serviços não precisam dar suporte a dispositivos de telefone.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivos de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921083"
---
# <a name="phone-devices"></a>Dispositivos de telefone

O suporte a dispositivos telefônicos é suplementar em vez de básico, portanto, os provedores de serviços não precisam dar suporte a dispositivos de telefone.

Assim como uma classe de dispositivo de linha é uma abstração de um dispositivo de linha físico, a classe de dispositivo de telefone representa uma abstração independente de dispositivo de um conjunto de telefone. A TAPI trata dispositivos de linha e telefone como dispositivos independentes um do outro. Em outras palavras, você pode usar um telefone (dispositivo) sem usar uma linha associada, e você pode usar uma linha (dispositivo) sem usar um telefone.

Provedores de serviços que implementam totalmente essa independência podem oferecer usos para esses dispositivos não definidos por protocolos de telefonia tradicionais. Por exemplo, uma pessoa pode usar o fone do telefone da área de trabalho como um dispositivo de áudio de forma de onda para gravação ou reprodução de voz, talvez sem o conhecimento do comutador de que o telefone está em uso. Nessa implementação, levantar o fone de telefone local não precisa enviar automaticamente um sinal offhook para o comutador.

Essa independência também permite que um aplicativo toque o telefone local de maneira independente das chamadas de entrada. Os recursos dos provedores de serviços são limitados pelos recursos do hardware e do software usados para interconectar o comutador, o telefone e o computador.

A TAPI inclui funções para recuperar recursos do dispositivo que permitem aos clientes determinar se esse modelo de uso tem suporte.

Esta seção descreve os dispositivos de telefone e explica como usar as funções de telefone TAPI para acessar esses dispositivos.

-   [Dispositivo de telefone](phone-device-elements.md)
-   [Inicialização e desligamento](initialization-and-shutdown.md)

 

 



