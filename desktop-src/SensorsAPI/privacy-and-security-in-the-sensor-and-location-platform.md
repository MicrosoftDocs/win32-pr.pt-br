---
description: A plataforma de sensor e localização do Windows inclui configurações de privacidade para ajudar a proteger as informações pessoais dos usuários.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacidade e segurança na plataforma de sensor e localização do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811282"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>Privacidade e segurança na plataforma de sensor e localização do Windows

A plataforma de sensor e localização do Windows inclui configurações de privacidade para ajudar a proteger as informações pessoais dos usuários.

A plataforma ajuda a garantir que os dados do sensor permaneçam privados, quando a privacidade é necessária, das seguintes maneiras:

-   Por padrão, os sensores estão desativados. Como o design da plataforma presume que qualquer sensor possa fornecer dados pessoais, cada sensor é desabilitado até que o usuário forneça consentimento explícito para acessar os dados do sensor.
-   O Windows fornece mensagens de divulgação e conteúdo de ajuda para o usuário. Esse conteúdo ajuda os usuários a entender como os sensores podem afetar a privacidade de seus dados pessoais e ajuda os usuários a tomar decisões informadas.
-   O fornecimento de permissão para um sensor requer direitos de administrador.
-   Quando habilitado, um dispositivo de sensor funciona para todos os programas em execução em uma conta de usuário específica (ou para todas as contas de usuário). Isso inclui usuários e serviços não interativos, como ASPNET ou SYSTEM. Por exemplo, se você habilitar um sensor de GPS para sua conta de usuário, somente os programas em execução na sua conta de usuário terão acesso ao GPS. Se você habilitar o GPS para todos os usuários, qualquer programa em execução em qualquer conta de usuário terá acesso ao GPS.
-   Os programas que usam sensores podem chamar um método para abrir uma caixa de diálogo do sistema que solicita que os usuários habilitem os dispositivos de sensor necessários. Esse recurso torna mais fácil para os desenvolvedores e usuários garantir que os sensores funcionem quando os programas precisarem, mantendo o controle de usuário de divulgação de dados de sensor.
-   Os drivers de sensor usam um objeto especial que processa todas as solicitações de e/s. Esse objeto garante que somente os programas que têm permissão de usuário possam acessar os dados do sensor.

 

 



