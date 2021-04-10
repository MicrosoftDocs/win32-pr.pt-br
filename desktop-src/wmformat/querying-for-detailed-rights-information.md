---
title: Consultando informações detalhadas sobre direitos
description: Consultando informações detalhadas sobre direitos
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- SDK do Windows Media Format, consultando direitos detalhados
- SDK do Windows Media Format, consultas de direitos detalhadas
- DRM (gerenciamento de direitos digitais), consultando direitos detalhados
- DRM (gerenciamento de direitos digitais), consultando direitos detalhados
- DRM (gerenciamento de direitos digitais), consultas de direitos detalhadas
- DRM (gerenciamento de direitos digitais), consultas de direitos detalhados
- APIs estendidas do cliente DRM, consultando direitos detalhados
- APIs estendidas do cliente, consultando direitos detalhados
- APIs estendidas do cliente DRM, consultas de direitos detalhadas
- APIs estendidas do cliente, consultas de direitos detalhadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159913"
---
# <a name="querying-for-detailed-rights-information"></a>Consultando informações detalhadas sobre direitos

Usando o método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , você pode obter informações detalhadas sobre os direitos concedidos por licenças para uma ID de chave. As informações obtidas desse método são agregadas de todas as licenças no armazenamento de licença local que se aplicam à ID de chave especificada.

**QueryLicenseState** usa a estrutura de [**\_ dados de \_ estado \_ da licença DRM**](drmdrm-license-state-data.md) para exibir informações de agregação sobre todas as licenças para a ID de chave especificada. Esse uso é diferente de outros objetos no SDK do Windows Media Format.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo informações de licenças no repositório de licenças local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




