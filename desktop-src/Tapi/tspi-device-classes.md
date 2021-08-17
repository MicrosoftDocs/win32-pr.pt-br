---
description: Saiba mais sobre classes de dispositivo TSPI. Uma classe de dispositivo é um grupo de dispositivos ou drivers de dispositivo por meio do qual os aplicativos enviam e recebem dados ou informações de chamada.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: Classes de dispositivo TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd6d2e79e021b6b73bc24ef0edb5b343fb8487ced3ca414084c7f2ad23a6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975432"
---
# <a name="tspi-device-classes"></a>Classes de dispositivo TSPI

Uma *classe de dispositivo* é um grupo de dispositivos físicos ou drivers de dispositivo relacionados por meio dos quais os aplicativos enviam e recebem as informações ou os dados que comiam uma chamada. Cada classe de dispositivo tem um nome de classe de dispositivo que identifica exclusivamente *a* classe e fornece informações sobre a interface de programação e comandos que podem ser usados para abrir e se comunicar com os dispositivos na classe .

A TAPI (Interface de Programação de Aplicativo de Telefonia) associa dispositivos de uma ou mais classes de dispositivo a cada linha ou dispositivo de telefone. Você acessa um desses dispositivos recuperando o identificador de dispositivo para o dispositivo usando a [**função lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) ou [**phoneGetID.**](/windows/win32/api/tapi/nf-tapi-phonegetid) Você fornece o nome da classe do dispositivo e a função retorna o nome da porta, o nome do dispositivo, o identificador do dispositivo ou o identificador de dispositivo específico que você precisa para abrir e acessar o dispositivo. O formato das informações retornadas depende da classe de dispositivo e é descrito nesta seção.

Você também usa nomes de classe de dispositivo com as funções [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) e [**phoneConfigDialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) para habilitar o usuário a definir opções de configuração para o dispositivo determinado; com as [**funções lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) e [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) para recuperar um ícone para representar o dispositivo determinado; e com as [**funções lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) e [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) para recuperar e definir opções de configuração diretamente para o dispositivo determinado.

A seguir estão os nomes de classe de dispositivo padrão.



| Nome da classe do dispositivo                                       | Descrição                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [Comunicação](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Porta de comunicações                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem por meio de uma porta de comunicação              |
| [comm/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Nome do dispositivo ao qual um modem está conectado |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Dispositivo de áudio wave (somente entrada)                   |
| [wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Dispositivo de áudio wave (somente saída)                  |
| [wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Dispositivo de áudio wave, duplex completo                   |
| [midi/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | Sequenciador MIDI (somente entrada)                      |
| [midi/out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | Sequenciador MIDI (somente saída)                     |
| [tapi/line](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Dispositivo de linha                                      |
| [tapi/phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Telefone dispositivo                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Dispositivo de rede                                   |
| [tapi/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Dispositivo terminal                                  |



 

Esses nomes não são sensíveis a maiúsculas e minúsculas, portanto, você pode usar qualquer combinação de letras maiúsculas e minúsculas.

Classes de dispositivo adicionais e nomes de classe de dispositivo podem estar disponíveis em um determinado sistema. Em geral, se um dispositivo não pertencer a uma das classes de dispositivo padrão, o fabricante normalmente definirá uma nova classe de dispositivo e atribuirá um nome de classe de dispositivo exclusivo. Você deve verificar a documentação do dispositivo para determinar quais classes de dispositivo adicionais estão disponíveis para ele. Observe, no entanto, que embora a classe de dispositivo e o tipo de mídia sejam relacionados, eles não são os mesmos. Um *tipo de* mídia descreve um formato de informações sobre uma chamada e uma classe de dispositivo define a interface de programação usada para gerenciar essas informações.  Portanto, mesmo que um fabricante defina um novo tipo de mídia, talvez não seja verdade que o fabricante também deve definir uma nova classe de dispositivo para dar suporte ao modo.

O formato dos dados de configuração usados com as funções [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) e [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) também depende da classe de dispositivo. Em geral, você usa **lineGetDevConfig** para salvar uma cópia dos dados de configuração do dispositivo atual e, em seguida, usa **lineSetDevConfig** com os dados de configuração salvos para restaurar a configuração do dispositivo para o estado anterior. Essa é uma maneira conveniente de alterar temporariamente a configuração sem exigir que o usuário a restaure manualmente para o estado anterior. Como o formato exato dos dados de configuração do dispositivo pode ser diferente com cada provedor de serviços, não use **lineSetDevConfig** e **lineGetDevConfig** para manipular os dados de configuração do dispositivo diretamente. Alguns formatos são fornecidos apenas para informações.

 

 
