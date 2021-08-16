---
title: Atalhos e variações de comando
description: Atalhos e variações de comando
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a3379b5eb6dced9ccebb3e04e76be87fdca7ea5af341b647cb0205888c283
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807916"
---
# <a name="command-shortcuts-and-variations"></a>Atalhos e variações de comando

Você pode usar vários atalhos ao trabalhar com comandos MCI. Esses atalhos permitem que você use um único identificador para se referir a todos os dispositivos [](open.md) que seu aplicativo abriu ou para abrir um dispositivo sem em emissão explícita de um comando aberto [**(MCI \_ OPEN).**](mci-open.md)

Você pode especificar "all" (MCI \_ ALL DEVICE ID) como um identificador de dispositivo para qualquer comando \_ \_ que não retorne informações. Quando você especifica "todos", a MCI envia o comando sequencialmente para todos os dispositivos abertos pelo aplicativo atual.

Por exemplo, o [**comando fechar**](close.md) "todos" fecha todos os dispositivos abertos e o comando [**reproduzir**](play.md) "todos" começa a reproduzir todos os dispositivos abertos pelo aplicativo. Como a MCI envia sequencialmente os comandos para os dispositivos MCI, há um intervalo entre quando o primeiro e o último dispositivo recebem o comando.

Usar "todos" é uma maneira conveniente de transmitir um comando para todos os seus dispositivos, mas você não deve confiar nele para sincronizar dispositivos; o tempo entre mensagens pode variar.

Ao emitir um comando e especificar um dispositivo que não está aberto, a MCI tenta abrir o dispositivo antes de implementar o comando. As seguintes regras se aplicam à abertura automática de dispositivos:

-   O recurso aberto automático funciona apenas com a interface de cadeia de caracteres de comando.
-   O recurso de abertura automática falha para comandos específicos para drivers de dispositivo personalizados.
-   Dispositivos abertos automaticamente não respondem a comandos que usam "todos" como um nome de dispositivo.
-   O recurso aberto automático não permite que seu aplicativo especifique o sinalizador "type". Sem o nome do dispositivo, a MCI determina o nome do dispositivo das entradas no Registro. Para usar um dispositivo específico, você pode combinar o nome do dispositivo com o nome do arquivo usando o ponto de exclamação, conforme descrito no material de referência para o [**comando open.**](open.md)

Se um aplicativo usar o recurso aberto automático para abrir um dispositivo, o aplicativo deverá verificar o valor de retorno de cada comando aberto subsequente para verificar se o dispositivo ainda está aberto. A MCI também fecha automaticamente qualquer dispositivo que ele abre automaticamente. A MCI normalmente fecha um dispositivo nas seguintes situações:

-   O comando foi concluído.
-   Você anula o comando.
-   Você solicita notificação em um comando subsequente.
-   A MCI detecta uma falha.

 

 




