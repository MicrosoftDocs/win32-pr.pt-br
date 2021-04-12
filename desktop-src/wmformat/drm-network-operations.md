---
title: Operações de rede DRM
description: Operações de rede DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- SDK do Windows Media Format, operações de rede DRM
- Formato de sistema avançado (ASF), operações de rede de DRM
- ASF (formato de sistemas avançados), operações de rede de DRM
- DRM (gerenciamento de direitos digitais), operações de rede
- DRM (gerenciamento de direitos digitais), operações de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291862"
---
# <a name="drm-network-operations"></a>Operações de rede DRM

Várias operações relacionadas ao DRM exigem que seu aplicativo se conecte a um serviço em execução em uma rede. Essas operações incluem individualização, aquisição de licença, revogação de licença e backup e restauração de licenças.

Assim como ocorre com qualquer transação de rede, seu aplicativo deve considerar uma variedade de dificuldades ao incluir recursos que exigem operações de rede. Seu aplicativo deve controlar o status da operação para qualquer extensão possível para o recurso específico, geralmente manipulando mensagens de status. Você deve fornecer comentários ao usuário sobre o status. Se uma operação falhar na primeira tentativa, você deverá dar ao usuário a oportunidade de tentar novamente. Em muitos casos, a primeira tentativa encontra dificuldade, mas uma tentativa subsequente é concluída sem erros.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




