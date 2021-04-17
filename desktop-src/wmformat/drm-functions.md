---
title: Funções do Microsoft Windows Media DRM Client
description: Funções do Microsoft Windows Media DRM Client
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- SDK do Windows Media Format, funções
- DRM (gerenciamento de direitos digitais), funções
- DRM (gerenciamento de direitos digitais), funções
- APIs estendidas do cliente DRM, funções
- APIs estendidas do cliente, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105782386"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funções do Microsoft Windows Media DRM Client

As funções a seguir são implementadas como parte das APIs estendidas do Microsoft Windows Media DRM Client.



| Função                                                             | Descrição                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Cria uma fábrica de classes que pode criar outros objetos DRM. Essa função não requer uma biblioteca de stub da Microsoft e cria objetos que não dão suporte aos recursos protegidos do DRM. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Cria uma fábrica de classes que pode criar outros objetos DRM. Essa função requer uma biblioteca de stub da Microsoft e cria objetos que dão suporte aos recursos protegidos do DRM.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Libera recursos usados pelas APIs.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inicializa os recursos usados pelas APIs.                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](drm-programming-reference.md)
</dt> </dl>

 

 




