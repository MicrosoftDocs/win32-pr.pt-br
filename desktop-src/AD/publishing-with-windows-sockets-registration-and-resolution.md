---
title: Publicação com a resolução Windows de soquetes & soquetes
description: Windows Os serviços de soquetes podem usar as APIs de Registro e Resolução (RnR) para publicar serviços e procurar serviços publicados com RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Registro de soquetes e AD de resolução, publicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a071a37d1d017e4c034f3eaab175889fdfcd1789d9f48aeac2c2943dfc8b4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184920"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Publicação com a resolução Windows de soquetes & soquetes

Windows Os serviços de soquetes podem usar as APIs de Registro e Resolução (RnR) para publicar serviços e procurar serviços publicados com RnR. A publicação RnR ocorre em duas etapas. A primeira etapa instala uma classe de serviço que associa um GUID a um nome para o serviço. A classe de serviço pode conter dados de configuração específicos do serviço. Os serviços podem publicar a si mesmos como instâncias da classe de serviço. Quando publicados, os clientes podem consultar o serviço de diretório para instâncias de uma determinada classe usando as APIs RnR e selecionar uma instância à qual se vincular. Quando uma classe não é mais necessária, ela pode ser removida.

 

 




