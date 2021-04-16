---
title: Publicando com a resolução de & de registro do Windows Sockets
description: O Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços e Pesquisar serviços publicados com o RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de registro e resolução do Windows Sockets, publicando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104453808"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Publicando com a resolução de & de registro do Windows Sockets

O Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços e Pesquisar serviços publicados com o RnR. A publicação RnR ocorre em duas etapas. A primeira etapa instala uma classe de serviço que associa um GUID com um nome para o serviço. A classe de serviço pode manter dados de configuração específicos do serviço. Os serviços podem, então, se publicar como instâncias da classe de serviço. Quando publicado, os clientes podem consultar o serviço de diretório em busca de instâncias de uma determinada classe usando as APIs RnR e selecionar uma instância à qual associar. Quando uma classe não é mais necessária, ela pode ser removida.

 

 




