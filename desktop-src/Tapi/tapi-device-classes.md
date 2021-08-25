---
description: Saiba mais sobre as classes de dispositivo TAPI. Uma classe de dispositivo é um grupo de dispositivos ou drivers de dispositivo por meio do qual os aplicativos enviam e recebem dados ou informações de chamada.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Classes de dispositivo TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f277e74012241139cf619c5229c4525711d93304f7321809461aff13416e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975476"
---
# <a name="tapi-device-classes"></a>Classes de dispositivo TAPI

Uma classe de dispositivo é um grupo de dispositivos físicos ou drivers de dispositivo relacionados por meio dos quais os aplicativos enviam e recebem as informações ou os dados que comiam uma chamada. Cada classe de dispositivo tem um nome de classe de dispositivo que identifica exclusivamente *a* classe e fornece informações sobre a interface de programação e comandos que podem ser usados para abrir e se comunicar com os dispositivos na classe .

A TAPI (Interface de Programação de Aplicativo de Telefonia) associa dispositivos de uma ou mais classes de dispositivo a cada linha ou dispositivo de telefone. Você acessa um desses dispositivos recuperando o identificador de dispositivo para o dispositivo usando a [**função lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) ou [**phoneGetID.**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) Você fornece o nome da classe do dispositivo e a função retorna o nome da porta, o nome do dispositivo, o identificador do dispositivo ou o identificador de dispositivo específico que você precisa para abrir e acessar o dispositivo. O formato das informações retornadas depende da classe de dispositivo e é descrito nos tópicos subsequentes desta seção.

Você também usa nomes de classe de dispositivo com as funções [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) para habilitar o usuário a definir opções de configuração para o dispositivo determinado, com as funções [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) para recuperar um ícone para representar o dispositivo determinado e com as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para recuperar e definir diretamente as opções de configuração para o dispositivo determinado.

A lista a seguir mostra os nomes de classe do dispositivo.



| Nome da classe do dispositivo                                      | Descrição                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [Comunicação](comm.md)                                       | Porta de comunicação.                              |
| [comm/datamodem](comm-datamodem.md)                   | Modem por meio de uma porta de comunicação.              |
| [comm/datamodem/portname](comm-datamodem-portname.md) | Nome do dispositivo ao qual um modem está conectado. |
| [wave/in](wave-in.md)                                 | Dispositivo de áudio wave (somente entrada).                   |
| [wave/out](wave-out.md)                               | Dispositivo de áudio wave (somente saída).                  |
| [wave/in/out](wave-in-out.md)                         | Dispositivo de áudio wave, full duplex.                   |
| [midi/in](midi-in.md)                                 | Sequenciador MIDI (somente entrada).                      |
| [midi/out](midi-out.md)                               | Sequenciador MIDI (somente saída).                     |
| [tapi/line](tapi-line.md)                             | Dispositivo de linha.                                      |
| [tapi/phone](tapi-phone.md)                           | Telefone dispositivo.                                     |
| [Ndis](ndis.md)                                       | Dispositivo de rede.                                   |
| [tapi/terminal](tapi-terminal.md)                     | Dispositivo terminal.                                  |



 

> [!Note]  
> Esses nomes não são sensíveis a minúsculas; você pode usar qualquer combinação de letras maiúsculas e minúsculas.

 

Classes de dispositivo adicionais e nomes de classe de dispositivo podem estar disponíveis em um determinado sistema. Em geral, se um dispositivo não pertencer a uma das classes de dispositivo padrão, o fabricante normalmente definirá uma nova classe de dispositivo e atribuirá um nome de classe de dispositivo exclusivo. Verifique a documentação do dispositivo para determinar quais classes de dispositivo adicionais estão disponíveis para ele. Observe, no entanto, que embora a classe de dispositivo e o tipo de mídia sejam relacionados, eles não são os mesmos. Um tipo de mídia descreve o formato de informações de chamada e uma classe de dispositivo define a interface de programação usada para gerenciar essas informações. Portanto, mesmo que um fabricante defina um novo tipo de mídia, não é necessariamente verdadeiro que o fabricante também precise definir uma nova classe de dispositivo para dar suporte ao modo.

O formato dos dados de configuração usados com as funções [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) também depende da classe de dispositivo. Em geral, você usa **lineGetDevConfig** para salvar uma cópia dos dados de configuração do dispositivo atual e, em seguida, usa **lineSetDevConfig** com os dados de configuração salvos para restaurar a configuração do dispositivo para o estado anterior. Essa é uma maneira conveniente de alterar temporariamente a configuração sem exigir que o usuário a restaure manualmente para o estado anterior. Como o formato exato dos dados de configuração do dispositivo pode ser diferente com cada provedor de serviços, você não deve usar **lineSetDevConfig** e **lineGetDevConfig** para manipular os dados de configuração do dispositivo diretamente. Alguns formatos são fornecidos apenas para informações.

 

 



