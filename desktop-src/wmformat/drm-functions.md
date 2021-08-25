---
title: Funções de cliente DRM Windows Mídia da Microsoft
description: Funções de cliente DRM Windows Mídia da Microsoft
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows SDK de Formato de Mídia, funções
- DRM (gerenciamento de direitos digitais), funções
- DRM (gerenciamento de direitos digitais), funções
- APIs estendidas do cliente DRM, funções
- APIs estendidas do cliente, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931166"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funções de cliente DRM Windows Mídia da Microsoft

As funções a seguir são implementadas como parte das APIs Estendidas do Cliente DRM do Microsoft Windows Media.



| Função                                                             | Descrição                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Cria uma fábrica de classes que pode criar os outros objetos DRM. Essa função não requer uma biblioteca de stub da Microsoft e cria objetos que não suportam os recursos de DRM protegidos. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Cria uma fábrica de classes que pode criar os outros objetos DRM. Essa função requer uma biblioteca de stub da Microsoft e cria objetos que suportam os recursos de DRM protegidos.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Libera os recursos usados pelas APIs.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inicializa os recursos usados pelas APIs.                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](drm-programming-reference.md)
</dt> </dl>

 

 




