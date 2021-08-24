---
title: Operações de rede DRM
description: Operações de rede DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows SDK de formato de mídia, operações de rede DRM
- ASF (Advanced Systems Format), operações de rede DRM
- ASF (Formato de Sistemas Avançados), operações de rede DRM
- DRM (gerenciamento de direitos digitais), operações de rede
- DRM (gerenciamento de direitos digitais), operações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f026ed972b88a1e6290bdd513012c2fab758da2c5b4b91a6a1162df5d258207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771746"
---
# <a name="drm-network-operations"></a>Operações de rede DRM

Várias operações relacionadas ao DRM exigem que seu aplicativo se conecte a um serviço em execução em uma rede. Essas operações incluem individualização, aquisição de licença, revogação de licença e restauração e backup de licença.

Assim como acontece com qualquer transação de rede, seu aplicativo deve levar em conta uma variedade de dificuldades ao incluir recursos que exigem operações de rede. Seu aplicativo deve acompanhar o status da operação para qualquer extensão possível para o recurso específico, geralmente manipulando mensagens de status. Você deve fornecer comentários ao usuário sobre o status. Se uma operação falhar na primeira tentativa, você deverá dar ao usuário a oportunidade de tentar novamente. Em muitos casos, a primeira tentativa encontra dificuldade, mas uma tentativa subsequente é concluída sem erro.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




