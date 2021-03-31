---
title: Instâncias de driver
description: Instâncias de driver
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- drivers instaláveis, instâncias
- drivers instaláveis, várias instâncias
- várias instâncias de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635598"
---
# <a name="driver-instances"></a>Instâncias de driver

O Windows permite várias instâncias de um driver instalável. O sistema cria uma instância do driver cada vez que o driver é aberto e destrói a instância quando o driver é fechado. As instâncias de driver são especialmente úteis para drivers instaláveis que dão suporte a vários dispositivos ou que são abertos por vários aplicativos ou pelo mesmo aplicativo várias vezes.

Para ajudar o driver a acompanhar as instâncias, o sistema envia um identificador de instância de driver com cada mensagem de driver após a criação da instância. Como esse identificador identifica exclusivamente a instância, os drivers instaláveis geralmente associam o identificador à memória e a outros recursos alocados especificamente para a instância.

Quando a primeira instância é aberta, o sistema envia as mensagens de [**\_ carregamento**](drv-load.md)do DRV, do [**drv \_ Enable**](drv-enable.md)e do [**drv \_**](drv-open.md) para o driver nessa ordem. As mensagens de carregamento de DRV \_ e drv \_ permitem notificar o driver de que ele está na memória e está habilitado para operação. A \_ mensagem drv Open identifica o identificador de instância e pode incluir informações de configuração para a instância. Em cada abertura subsequente de uma instância do mesmo Driver, o sistema envia somente uma mensagem DRV \_ Open.

Ao processar uma mensagem de carregamento de DRV \_ , um driver normalmente lê as definições de configuração do registro, configura o driver e qualquer hardware associado e aloca memória para uso por todas as instâncias do driver. Se um driver não puder concluir a configuração ou alocar memória, ele retornará zero para instruir o sistema a remover imediatamente o driver da memória e impedir que todas as mensagens subsequentes sejam enviadas. Ao processar a \_ mensagem de habilitação de DRV, o driver prepara o hardware para receber e processar solicitações de e/s (entrada e saída). A preparação pode incluir a instalação de manipuladores de interrupção.

Ao processar a mensagem de abertura do DRV \_ , o driver aloca memória ou recursos exigidos pela instância específica do driver e retorna um valor diferente de zero. O sistema usa esse valor diferente de zero como o *identificador de driver* em mensagens de driver subsequentes para a instância. O driver pode usar esse identificador para qualquer finalidade. Por exemplo, alguns drivers usam um identificador de memória para o identificador para obter acesso rápido à memória que contém informações sobre a instância especificada.

Muitos drivers instaláveis processam o segundo parâmetro da \_ mensagem drv Open, dando ao sistema e aos aplicativos o meio de enviar informações adicionais ao driver ao abrir uma instância. O parâmetro pode ser um único valor ou um endereço de uma estrutura que contém um conjunto de valores. Ao processar \_ o DRV Open, o driver verifica o parâmetro para determinar se ele é um valor e usa os valores especificados, se houver, para concluir a criação da instância.

O sistema envia uma mensagem de [**\_ fechamento drv**](drv-close.md) cada vez que uma instância é fechada. O identificador de instância enviado com a mensagem identifica qual instância deve ser fechada. Quando a última instância restante é fechada, o sistema envia as \_ mensagens de fechamento DRV, [**drv \_ Disable**](drv-disable.md)e [**drv \_ Free**](drv-free.md) nessa ordem. A \_ mensagem de fechamento drv direciona o driver para fechar a instância e as mensagens de \_ desativação drv Disable e drv \_ Free notificam o driver de que ele está desabilitado e será imediatamente liberado da memória.

Ao processar a \_ mensagem de fechamento DRV, o driver normalmente libera memória ou recursos alocados para a instância. Ao processar a \_ mensagem de desabilitação de DRV, o driver coloca qualquer hardware em um estado inativo, o que pode incluir a remoção de manipuladores de interrupção. Ao processar a \_ mensagem drv Free, o driver libera a memória ou os recursos que ainda estão alocados.

Os drivers instaláveis não são necessários para dar suporte a várias instâncias. Um driver pode impedir que qualquer instância seja criada retornando zero para a mensagem de [**\_ abertura de drv**](drv-open.md) .

 

 




