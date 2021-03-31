---
title: Atalhos de comando e variações
description: Atalhos de comando e variações
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636578"
---
# <a name="command-shortcuts-and-variations"></a>Atalhos de comando e variações

Você pode usar vários atalhos ao trabalhar com comandos MCI. Esses atalhos permitem que você use um único identificador para se referir a todos os dispositivos que seu aplicativo abriu ou para abrir um dispositivo sem emitir explicitamente um comando [**aberto**](open.md) ([**MCI \_ Open**](mci-open.md)).

Você pode especificar "todos" (MCI \_ todos \_ os \_ ID do dispositivo) como um identificador de dispositivo para qualquer comando que não retorna informações. Quando você especifica "All", o MCI envia o comando sequencialmente para todos os dispositivos abertos pelo aplicativo atual.

Por exemplo, o comando [**fechar**](close.md) "todos" fecha todos os dispositivos abertos e o comando [**reproduzir**](play.md) "todos" começa a reproduzir todos os dispositivos abertos pelo aplicativo. Como o MCI envia seqüencialmente os comandos para os dispositivos MCI, há um intervalo entre quando o primeiro e último dispositivos recebem o comando.

Usar "All" é uma maneira conveniente de transmitir um comando para todos os seus dispositivos, mas você não deve confiar nele para sincronizar dispositivos; o intervalo entre as mensagens pode variar.

Quando você emite um comando e especifica um dispositivo que não está aberto, o MCI tenta abrir o dispositivo antes de implementar o comando. As regras a seguir se aplicam para abrir dispositivos automaticamente:

-   O recurso abrir automático funciona apenas com a interface de cadeia de caracteres de comando.
-   O recurso aberto automático falha para comandos específicos de drivers de dispositivo personalizados.
-   Os dispositivos abertos automaticamente não respondem a comandos que usam "todos" como um nome de dispositivo.
-   O recurso aberto automático não permite que seu aplicativo especifique o sinalizador "tipo". Sem o nome do dispositivo, o MCI determina o nome do dispositivo nas entradas no registro. Para usar um dispositivo específico, você pode combinar o nome do dispositivo com o nome do arquivo usando o ponto de exclamação, conforme descrito no material de referência do comando [**abrir**](open.md) .

Se um aplicativo usar o recurso abrir automaticamente para abrir um dispositivo, o aplicativo deverá verificar o valor de retorno de cada comando Open subsequente para verificar se o dispositivo ainda está aberto. O MCI também fecha automaticamente qualquer dispositivo que abrir automaticamente. O MCI normalmente fecha um dispositivo nas seguintes situações:

-   O comando está concluído.
-   Você anula o comando.
-   Você solicita uma notificação em um comando subsequente.
-   O MCI detecta uma falha.

 

 




