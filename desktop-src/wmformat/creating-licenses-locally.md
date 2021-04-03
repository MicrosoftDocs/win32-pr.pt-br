---
title: Criando licenças localmente
description: Criando licenças localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- SDK do Windows Media Format, criando licenças localmente
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, criando licenças localmente
- APIs estendidas do cliente, criando licenças localmente
- licenças, criando licenças localmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006137"
---
# <a name="creating-licenses-locally"></a>Criando licenças localmente

Em determinadas circunstâncias, como durante a [importação de DRM](drm-import.md), você pode criar suas próprias licenças. As licenças do Windows Media DRM podem ser escritas de algumas maneiras diferentes, mas para fazer sua própria licença, você deve usar o esquema binário XMR (direitos de mídia extensível). Para obter mais informações, consulte [criando uma licença do XMR](building-an-xmr-license.md).

Ao criar uma licença, você pode adicioná-la ao repositório de licenças local chamando o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirindo licenças**](acquiring-licenses.md)
</dt> <dt>

[**Criando uma licença do XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




