---
description: Uma classe de dispositivo é um grupo de dispositivos físicos ou drivers de dispositivo relacionados por meio dos quais os aplicativos enviam e recebem as informações ou os dados que compõem uma chamada.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Classes de dispositivo TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10392487657e8190052546605c54bed8cc0ccf4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297579"
---
# <a name="tspi-device-classes"></a>Classes de dispositivo TSPI

Uma *classe de dispositivo* é um grupo de dispositivos físicos ou drivers de dispositivo relacionados por meio dos quais os aplicativos enviam e recebem as informações ou os dados que compõem uma chamada. Cada classe de dispositivo tem um *nome de classe de dispositivo* que identifica exclusivamente a classe e fornece informações sobre a interface de programação e os comandos que podem ser usados para abrir e se comunicar com os dispositivos na classe.

A TAPI (interface de programação de aplicativos de telefonia) associa dispositivos de uma ou mais classes de dispositivo a cada linha ou dispositivo de telefone. Você acessa um desses dispositivos recuperando o identificador do dispositivo para o dispositivo usando a função [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) ou [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) . Você fornece o nome da classe do dispositivo e a função retorna o nome da porta específica, o nome do dispositivo, o identificador do dispositivo ou a identificação do dispositivo que você precisa abrir e acessar o dispositivo. O formato das informações retornadas depende da classe do dispositivo e é descrito nesta seção.

Você também usa nomes de classe de dispositivo com as funções [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) para permitir que o usuário defina as opções de configuração para o dispositivo especificado; com as funções [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) para recuperar um ícone que representa o dispositivo determinado; e com as funções [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) para recuperar e definir diretamente as opções de configuração para o dispositivo especificado.

A seguir estão os nomes de classe de dispositivo padrão.



| Nome da classe do dispositivo                                       | Descrição                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [Comentários](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Porta de comunicação                              |
| [comm/datamodeto](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem por meio de uma porta de comunicação              |
| [comm/datamodeling/PortName](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nome do dispositivo ao qual um modem está conectado |
| [onda/entrada](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo de áudio Wave (somente entrada)                   |
| [Wave/saída](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo de áudio Wave (somente saída)                  |
| [Wave/entrada/saída](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo de áudio Wave, full duplex                   |
| [MIDI/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | Sequencer MIDI (somente entrada)                      |
| [MIDI/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | Sequenciador MIDI (somente saída)                     |
| [TAPI/linha](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo de linha                                      |
| [TAPI/telefone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Dispositivo de telefone                                     |
| [recepção](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo de rede                                   |
| [TAPI/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo de terminal                                  |



 

Esses nomes não diferenciam maiúsculas de minúsculas, portanto, você pode usar qualquer combinação de letras maiúsculas e minúsculas.

Classes de dispositivo e nomes de classe de dispositivo adicionais podem estar disponíveis em um determinado sistema. Em geral, se um dispositivo não pertencer a uma das classes de dispositivo padrão, o fabricante normalmente define uma nova classe de dispositivo e atribui um nome de classe de dispositivo exclusivo. Você deve verificar a documentação do dispositivo para determinar quais classes de dispositivo adicionais estão disponíveis para ele. No entanto, observe que, embora a classe de dispositivo e o tipo de mídia estejam relacionados, eles não são os mesmos. Um *tipo de mídia* descreve um formato de informações em uma chamada, e uma *classe de dispositivo* define a interface de programação usada para gerenciar essas informações. Portanto, mesmo que um fabricante defina um novo tipo de mídia, talvez não seja verdade que o fabricante também deve definir uma nova classe de dispositivo para dar suporte ao modo.

O formato dos dados de configuração usados com as funções [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) também depende da classe de dispositivo. Em geral, você usa **lineGetDevConfig** para salvar uma cópia dos dados de configuração do dispositivo atual e, posteriormente, usar o **lineSetDevConfig** com os dados de configuração salvos para restaurar a configuração do dispositivo para o estado anterior. Essa é uma maneira conveniente de alterar temporariamente a configuração sem exigir que o usuário a restaure manualmente para o estado anterior. Como o formato exato dos dados de configuração do dispositivo pode ser diferente com cada provedor de serviços, não use **lineSetDevConfig** e **lineGetDevConfig** para manipular diretamente os dados de configuração do dispositivo. Alguns formatos são fornecidos apenas para fins informativos.

 

 
