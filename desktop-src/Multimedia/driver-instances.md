---
title: Instâncias de driver
description: Instâncias de driver
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- drivers instanciados, instâncias
- drivers instanciados, várias instâncias
- várias instâncias de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deea546ffb7cd848993f8aac569d3624f87988b583ea47cab7bb16451cc6ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941193"
---
# <a name="driver-instances"></a>Instâncias de driver

Windows permite várias instâncias de um driver instanciado. O sistema cria uma instância do driver sempre que o driver é aberto e destrói a instância quando o driver é fechado. As instâncias de driver são especialmente úteis para drivers instanciados que suportam vários dispositivos ou que são abertos por vários aplicativos ou pelo mesmo aplicativo várias vezes.

Para ajudar o driver a controlar as instâncias, o sistema envia um handle de instância de driver com cada mensagem de driver após a criação da instância. Como esse identificador identifica exclusivamente a instância, drivers instanciados geralmente associam o identificador à memória e a outros recursos alocados especificamente para a instância.

Quando a primeira instância é aberta, o sistema envia as mensagens [**DRV \_ LOAD,**](drv-load.md) [**DRV \_ ENABLE**](drv-enable.md)e [**DRV \_ OPEN**](drv-open.md) para o driver nessa ordem. As mensagens DRV \_ LOAD e DRV ENABLE notificam o driver de que ele agora está na \_ memória e está habilitado para operação. A mensagem DRV \_ OPEN identifica o identificador de instância e pode incluir informações de configuração para a instância. Em cada abertura subsequente de uma instância do mesmo driver, o sistema envia apenas uma mensagem DRV \_ OPEN.

Ao processar uma mensagem LOAD DRV, um driver normalmente lê as definições de configuração do Registro, configura o driver e qualquer hardware associado e aloca memória para uso por todas as instâncias do \_ driver. Se um driver não puder concluir a configuração ou alocar memória, ele retornará zero para direcionar o sistema a remover imediatamente o driver da memória e impedir que as mensagens subsequentes seja enviadas. Ao processar a mensagem HABILITAR DRV, o driver prepara o hardware para receber e processar solicitações de entrada e saída \_ (E/S). A preparação pode incluir a instalação de manipuladores de interrupção.

Ao processar a mensagem DRV OPEN, o driver aloca memória ou recursos exigidos pela instância determinada do driver e retorna um valor não \_ zero. O sistema usa esse valor não zero como o *identificador de driver* nas mensagens de driver subsequentes para a instância. O driver pode usar esse identificador para qualquer finalidade. Por exemplo, alguns drivers usam um identificador de memória para o identificador para obter acesso rápido à memória que contém informações sobre a instância determinada.

Muitos drivers instanciados processam o segundo parâmetro da mensagem DRV OPEN, dando ao sistema e aos aplicativos os meios para enviar informações adicionais ao driver ao \_ abrir uma instância. O parâmetro pode ser um único valor ou um endereço de uma estrutura que contém um conjunto de valores. Ao processar DRV OPEN, o driver verifica o parâmetro para determinar se ele é um valor e usa os valores determinados, se algum, para concluir a criação \_ da instância.

O sistema envia uma [**mensagem DRV \_ CLOSE**](drv-close.md) sempre que uma instância é fechada. O identificador de instância enviado com a mensagem identifica qual instância fechar. Quando a última instância restante é fechada, o sistema envia as mensagens DRV \_ CLOSE, [**DRV \_ DISABLE**](drv-disable.md)e [**DRV \_ FREE**](drv-free.md) nessa ordem. A mensagem DRV CLOSE direciona o driver para fechar a instância e as mensagens DRV DISABLE e DRV FREE notificam o driver de que ele agora está desabilitado e será imediatamente \_ \_ liberado da \_ memória.

Ao processar a mensagem DRV CLOSE, o driver normalmente libera qualquer memória ou recursos \_ alocados para a instância. Ao processar a mensagem DRV DISABLE, o driver coloca qualquer hardware em um estado inativo, o que pode incluir a remoção de \_ manipuladores de interrupção. Ao processar a mensagem DRV FREE, o driver libera qualquer memória ou recursos \_ que ainda estão alocados.

Drivers instanciados não são necessários para dar suporte a várias instâncias. Um driver pode impedir que qualquer instância seja criada retornando zero para a [**mensagem DRV \_ OPEN.**](drv-open.md)

 

 




