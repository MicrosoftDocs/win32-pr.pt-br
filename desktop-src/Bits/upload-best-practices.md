---
title: Práticas recomendadas de upload
description: Highloads pode causar várias condições de tempo limite do servidor, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004965"
---
# <a name="upload-best-practices"></a>Práticas recomendadas de upload

Highloads pode causar várias condições de tempo limite do servidor, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente. Além disso, um grande número de conexões pendentes consumirá mais recursos do servidor e tornará a situação pior. Além disso, se o aplicativo de back-end não for gravado para lidar com condições de alta carga, ele poderá falhar ou se comportar. O aplicativo deve executar as etapas a seguir para limitar a carga no back-end.

Se o aplicativo do servidor não for gravado para lidar com grandes volumes, podem ocorrer condições de tempo limite, o que pode, por sua vez, aumentar a carga quando o cliente tentar novamente. Além disso, um grande número de conexões pendentes consumirá mais recursos do servidor.

Ao testar o aplicativo de servidor, teste com a carga mais alta possível. Você deve usar vários computadores cliente, cada um com vários trabalhos simultâneos do BITS de primeiro plano e medir a taxa de transferência máxima no back-end. Se não for possível medir a taxa de transferência, você precisará estimar a taxa de transferência.

O aplicativo de servidor deve residir em uma URL diferente da URL de carregamento (consulte a propriedade do IIS do BITS, **BITSServerNotificationURL**).

É uma boa prática limitar a carga no servidor de aplicativos com base nos valores de taxa de transferência comprovados. Você deve usar as propriedades do IIS, **MaxBandwidth** e **MaxConnections**, para limitar a carga no servidor de aplicativos.

 

 




