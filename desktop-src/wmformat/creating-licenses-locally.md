---
title: Criando licenças localmente
description: Criando licenças localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows SDK de Formato de Mídia, criando licenças localmente
- Windows SDK de Formato de Mídia, licenças
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs Estendidas do Cliente DRM, criando licenças localmente
- APIs estendidas do cliente, criando licenças localmente
- licenças, criando licenças localmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1a889e83f093cbd60043b299b7174a6c963663962a66454c5707060e76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433902"
---
# <a name="creating-licenses-locally"></a>Criando licenças localmente

Em determinadas circunstâncias, como durante a [Importação de DRM,](drm-import.md)você pode criar suas próprias licenças. Windows As licenças de DRM de mídia podem ser escritas de algumas maneiras diferentes, mas para fazer sua própria licença, você deve usar o esquema binário XMR (Extensible Media Rights). Para obter mais informações, consulte [Criando uma licença XMR.](building-an-xmr-license.md)

Ao criar uma licença, você pode adicioná-la ao armazenamento de licenças local chamando o método [**IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirir licenças**](acquiring-licenses.md)
</dt> <dt>

[**Criando uma licença XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




