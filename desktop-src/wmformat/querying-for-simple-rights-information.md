---
title: Consultando informações de direitos simples
description: Consultando informações de direitos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows SDK de Formato de Mídia, consultando direitos simples
- Windows SDK de Formato de Mídia, consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- APIs Estendidas do Cliente DRM, consultando direitos simples
- APIs estendidas do cliente, consultando direitos simples
- APIs estendidas do cliente DRM, consultas de direitos simples
- APIs estendidas do cliente, consultas de direitos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0686616bbc700c51a005c3e1e63eed889c42965aaebbba232fcf90b9cce26987
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027364"
---
# <a name="querying-for-simple-rights-information"></a>Consultando informações de direitos simples

As APIs estendidas do cliente drm de Windows mídia permitem que você receba rapidamente informações simples sobre se o conteúdo protegido pode ser acessado para várias ações.

O [**método IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pode ser usado para determinar rapidamente se uma ação é permitida por uma licença no armazenamento de licenças local. **QueryActionAllowed** foi otimizado para ser muito mais rápido do que consultas para obter informações semelhantes usando os objetos do SDK Windows Formato de Mídia. No entanto, esse tipo de consulta agrega as licenças no armazenamento de licenças local e deve ser usado somente para recursos simples, como pode ser necessário para elementos de interface do usuário, por exemplo, exibindo um indicador de permissão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obter informações de licenças no armazenamento de licenças local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




