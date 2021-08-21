---
description: Sensores lógicos fornecem dados sem depender de dispositivos de hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Sobre sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bb7a6e67223bb959b155e55f6cc059ffd8280bc8c08fb00d4d88cb2c8b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003885"
---
# <a name="about-logical-sensors"></a>Sobre sensores lógicos

*Sensores lógicos* fornecem dados sem depender de dispositivos de hardware. Por exemplo, um sensor lógico pode fornecer dados sobre o local atual do usuário usando um serviço que pesquisa um endereço IP em uma tabela. Sensores lógicos são implementados como drivers de sensor. Para obter informações sobre como implementar um driver de sensor, consulte o Windows Driver Kit.

Depois que um sensor lógico é instalado no computador do usuário, você pode usá-lo da mesma maneira que um sensor baseado em hardware. A API do Sensor fornecerá uma interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) para representar o sensor lógico e seu programa pode solicitar dados por meio dos mesmos mecanismos que você usaria para qualquer outro tipo de sensor. Os sensores lógicos também podem usar as categorias, tipos, tipos de dados, propriedades e eventos definidos pela plataforma. Ou você pode definir valores personalizados.

A interface [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) permite que os desenvolvedores que criam sensores lógicos gerenciem conexões com a plataforma Sensor e Local.

> [!Note]  
> Assim como com outros drivers, instalar ou desinstalar um driver de sensor lógico requer privilégios de administrador.

 

Para tentar usar um sensor lógico de exemplo, consulte [Sobre as Amostras e Ferramentas](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Gerenciando sensores lógicos

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) tem os seguintes métodos:

-   [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Desconectar**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Desinstalar**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Quando você chama [**Conexão**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), a API do Sensor cria uma instância do driver do sensor, se ainda não existir, e conecta o sensor lógico à plataforma. Isso significa que o sensor lógico aparece com outros sensores no **Sensor de Localização e Outros Sensores** Painel de Controle. Quando você [](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))chama Desconectar , a API do Sensor desconecta o sensor lógico e o remove do Painel de Controle. Chamar **Desconectar** não remove o sensor lógico **do Gerenciador de Dispositivos**. Portanto, chamadas futuras **para Conexão** resultarão em uma conexão muito mais rápida com o sensor lógico.

Para remover um sensor lógico, você deve chamar [**Desinstalar**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). Desinstalar um sensor lógico remove o sensor **do Gerenciador de Dispositivos**. Como os dispositivos de sensor lógico existem apenas na memória, um sensor lógico é desinstalado quando o usuário reinicia Windows.

A API do Sensor identifica um sensor lógico específico por sua *ID lógica*, que é um **GUID.** Sempre que você se conectar a um sensor lógico específico, deverá fornecer uma ID lógica. Sempre que você desconectar ou desinstalar um sensor específico, deverá fornecer a mesma ID lógica usada para se conectar. Se você se conectar ao mesmo driver de sensor lógico várias vezes usando IDs lógicas diferentes, criará uma instância separada do sensor lógico para cada nova ID lógica. Mesmo se [](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) você chamar Desconectar para cada ID lógica, essas [](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) instâncias separadas permanecerão no **Gerenciador de Dispositivos** até que você chame Desinstalar para cada sensor lógico ou o usuário reinicie Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando sensores lógicos](using-logical-sensors.md)
</dt> </dl>

 

 
