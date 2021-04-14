---
description: Uma difusão geral através da Internet é obtida definindo os campos SA \_ netnum e SA \_ nodenum para os binários (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difusão de todas as rotas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461120"
---
# <a name="all-routes-broadcast"></a>Difusão de todas as rotas

Uma difusão geral através da Internet é obtida definindo os campos **SA \_ netnum** e **SA \_ nodenum** para os binários (1). O provedor de serviços Converte essa solicitação em um pacote de tipo 20, que os roteadores IPX reconhecem e encaminham. O pacote visita todas as sub-redes e pode ser duplicado várias vezes. Os receptores devem lidar com várias cópias duplicadas do datagrama.

O uso desse tipo de difusão não é popular entre os administradores de rede, portanto, seu uso deve ser extremamente limitado. Muitos roteadores desativam esse tipo de difusão, deixando partes da sub-rede invisíveis para o pacote.

 

 



