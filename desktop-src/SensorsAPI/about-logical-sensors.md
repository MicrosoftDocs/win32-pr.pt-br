---
description: Os sensores lógicos fornecem dados sem depender de dispositivos de hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Sobre sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769187"
---
# <a name="about-logical-sensors"></a>Sobre sensores lógicos

Os *sensores lógicos* fornecem dados sem depender de dispositivos de hardware. Por exemplo, um sensor lógico pode fornecer dados sobre o local atual do usuário usando um serviço que pesquisa um endereço IP em uma tabela. Sensores lógicos são implementados como drivers de sensor. Para obter informações sobre como implementar um driver de sensor, consulte o kit de driver do Windows.

Depois que um sensor lógico é instalado no computador do usuário, você pode usá-lo da mesma maneira que um sensor baseado em hardware. A API do sensor fornecerá uma interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) para representar o sensor lógico e seu programa poderá solicitar dados por meio dos mesmos mecanismos que você usaria para qualquer outro tipo de sensor. Sensores lógicos também podem usar as categorias de sensor, tipos, tipos de dados, propriedades e eventos definidos pela plataforma. Ou você pode definir valores personalizados.

A interface [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) permite que os desenvolvedores criem sensores lógicos para gerenciar conexões com o sensor e a plataforma de localização.

> [!Note]  
> Assim como ocorre com outros drivers, instalar ou desinstalar um driver de sensor lógico requer privilégios de administrador.

 

Para tentar usar um sensor lógico de exemplo, consulte [sobre os exemplos e as ferramentas](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Gerenciando sensores lógicos

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) tem os seguintes métodos:

-   [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Desconectar**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Desinstalar**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Quando você chamar [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), a API do sensor criará uma instância do driver do sensor, se ainda não existir uma, e conectará o sensor lógico à plataforma. Isso significa que o sensor lógico aparece com outros sensores no painel de controle **local e outros sensores** . Quando você chama [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), a API do sensor desconecta o sensor lógico e o Remove do painel de controle. A chamada para **Desconectar** não remove o sensor lógico do **Gerenciador de dispositivos**. Portanto, chamadas futuras para **conexão** resultarão em uma conexão muito mais rápida com o sensor lógico.

Para remover um sensor lógico, você deve chamar [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). A desinstalação de um sensor lógico remove o sensor do **Gerenciador de dispositivos**. Como os dispositivos de sensor lógico existem apenas na memória, um sensor lógico é desinstalado quando o usuário reinicia o Windows.

A API do sensor identifica um determinado sensor lógico por sua *ID lógica*, que é um **GUID**. Sempre que se conectar a um sensor lógico específico, você deverá fornecer uma ID lógica. Sempre que você desconectar ou desinstalar um sensor específico, deverá fornecer a mesma ID lógica usada para se conectar. Se você se conectar ao mesmo driver de sensor lógico várias vezes usando diferentes IDs lógicas, você criará uma instância separada do sensor lógico para cada nova ID lógica. Mesmo que você chame [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) para cada ID lógica, essas instâncias separadas permanecerão em **Gerenciador de dispositivos** até que você chame [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) para cada sensor lógico ou o usuário reinicie o Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando sensores lógicos](using-logical-sensors.md)
</dt> </dl>

 

 
