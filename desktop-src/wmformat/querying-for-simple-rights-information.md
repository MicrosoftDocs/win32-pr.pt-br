---
title: Consultando informações de direitos simples
description: Consultando informações de direitos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- SDK do Windows Media Format, consultando direitos simples
- SDK do Windows Media Format, consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- APIs estendidas do cliente DRM, consultando direitos simples
- APIs estendidas do cliente, consultando direitos simples
- APIs estendidas do cliente DRM, consultas de direitos simples
- APIs estendidas do cliente, consultas de direitos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364014"
---
# <a name="querying-for-simple-rights-information"></a>Consultando informações de direitos simples

As APIs estendidas do cliente DRM do Windows Media permitem que você obtenha rapidamente informações simples sobre se o conteúdo protegido pode ser acessado para várias ações.

O método [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pode ser usado para determinar rapidamente se uma ação é permitida por uma licença no repositório de licenças local. O **QueryActionAllowed** foi otimizado para ser muito mais rápido do que as consultas de informações semelhantes usando os objetos do SDK do Windows Media Format. No entanto, esse tipo de consulta agrega as licenças no repositório de licenças local e deve ser usado somente para recursos simples, como pode ser necessário para elementos da interface do usuário, por exemplo, exibindo um indicador de permissão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo informações de licenças no repositório de licenças local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




