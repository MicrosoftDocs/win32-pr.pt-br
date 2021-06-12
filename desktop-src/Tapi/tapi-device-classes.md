---
description: Saiba mais sobre as classes de dispositivo TAPI. Uma classe de dispositivo é um grupo de dispositivos ou drivers de dispositivo por meio dos quais os aplicativos enviam e recebem informações de chamada ou dados.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: Classes de dispositivo TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c16f5baf81bdc66d5110da2a1ac5127237738e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011359"
---
# <a name="tapi-device-classes"></a>Classes de dispositivo TAPI

Uma classe de dispositivo é um grupo de dispositivos físicos ou drivers de dispositivo relacionados por meio dos quais os aplicativos enviam e recebem as informações ou os dados que compõem uma chamada. Cada classe de dispositivo tem um *nome de classe de dispositivo* que identifica exclusivamente a classe e fornece informações sobre a interface de programação e os comandos que podem ser usados para abrir e se comunicar com os dispositivos na classe.

A TAPI (interface de programação de aplicativos de telefonia) associa dispositivos de uma ou mais classes de dispositivo a cada linha ou dispositivo de telefone. Você acessa um desses dispositivos recuperando o identificador do dispositivo para o dispositivo usando a função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) ou [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) . Você fornece o nome da classe do dispositivo e a função retorna o nome da porta específica, o nome do dispositivo, o identificador do dispositivo ou a identificação do dispositivo que você precisa abrir e acessar o dispositivo. O formato das informações retornadas depende da classe do dispositivo e é descrito nos tópicos subsequentes desta seção.

Você também usa nomes de classe de dispositivo com as funções [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) para permitir que o usuário defina opções de configuração para o dispositivo fornecido, com as funções [**lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) para recuperar um ícone para representar o dispositivo fornecido e com as funções [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) para recuperar e definir as opções de configuração diretamente para o dispositivo especificado.

A lista a seguir mostra os nomes de classe de dispositivo.



| Nome da classe do dispositivo                                      | Descrição                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [Comentários](comm.md)                                       | Porta de comunicação.                              |
| [comm/datamodeto](comm-datamodem.md)                   | Modem por meio de uma porta de comunicação.              |
| [comm/datamodeling/PortName](comm-datamodem-portname.md) | Nome do dispositivo ao qual um modem está conectado. |
| [onda/entrada](wave-in.md)                                 | Dispositivo de áudio Wave (somente entrada).                   |
| [Wave/saída](wave-out.md)                               | Dispositivo de áudio Wave (somente saída).                  |
| [Wave/entrada/saída](wave-in-out.md)                         | Dispositivo de áudio Wave, full duplex.                   |
| [MIDI/in](midi-in.md)                                 | Sequenciador MIDI (somente entrada).                      |
| [MIDI/out](midi-out.md)                               | Sequenciador MIDI (somente saída).                     |
| [TAPI/linha](tapi-line.md)                             | Dispositivo de linha.                                      |
| [TAPI/telefone](tapi-phone.md)                           | Dispositivo de telefone.                                     |
| [recepção](ndis.md)                                       | Dispositivo de rede.                                   |
| [TAPI/terminal](tapi-terminal.md)                     | Dispositivo de terminal.                                  |



 

> [!Note]  
> Esses nomes não diferenciam maiúsculas de minúsculas; Você pode usar qualquer combinação de letras maiúsculas e minúsculas.

 

Classes de dispositivo e nomes de classe de dispositivo adicionais podem estar disponíveis em um determinado sistema. Em geral, se um dispositivo não pertencer a uma das classes de dispositivo padrão, o fabricante normalmente define uma nova classe de dispositivo e atribui um nome de classe de dispositivo exclusivo. Verifique a documentação do dispositivo para determinar quais classes de dispositivo adicionais estão disponíveis para ele. No entanto, observe que, embora a classe de dispositivo e o tipo de mídia estejam relacionados, eles não são os mesmos. Um tipo de mídia descreve o formato de informações de chamada e uma classe de dispositivo define a interface de programação usada para gerenciar essas informações. Portanto, mesmo que um fabricante defina um novo tipo de mídia, não é necessariamente verdadeiro que o fabricante também precise definir uma nova classe de dispositivo para dar suporte ao modo.

O formato dos dados de configuração usados com as funções [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) também depende da classe de dispositivo. Em geral, você usa **lineGetDevConfig** para salvar uma cópia dos dados de configuração do dispositivo atual e, posteriormente, usar o **lineSetDevConfig** com os dados de configuração salvos para restaurar a configuração do dispositivo para o estado anterior. Essa é uma maneira conveniente de alterar temporariamente a configuração sem exigir que o usuário a restaure manualmente para o estado anterior. Como o formato exato dos dados de configuração do dispositivo pode ser diferente com cada provedor de serviços, você não deve usar **lineSetDevConfig** e **lineGetDevConfig** para manipular diretamente os dados de configuração do dispositivo. Alguns formatos são fornecidos apenas para informações.

 

 



