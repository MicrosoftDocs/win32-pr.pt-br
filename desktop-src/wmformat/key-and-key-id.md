---
title: Chave e ID da chave
description: Chave e ID da chave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows SDK de Formato de Mídia, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), KID
- DRM (gerenciamento de direitos digitais),KID
- ID da chave (KID)
- KID (ID da chave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae448cd0c973ad11b55df6365039240ebe2c6ebadb3eda5f70b7f8dd1bfbfbc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929956"
---
# <a name="key-and-key-id"></a>Chave e ID da chave

Ao empacotar um arquivo, você usa uma chave. Uma chave é uma parte dos dados usados nos algoritmos de criptografia que protegem o conteúdo. Há duas partes para cada chave: uma semente de chave de licença e uma ID de chave (geralmente abreviada como KID). A ID da chave é pública e é armazenada no header do arquivo como uma maneira de identificar a chave necessária para descriptografar o arquivo. A semente da chave de licença é um valor secreto que deve ser compartilhado pelo empacotador de conteúdo e pelo emissor da licença.

Uma ID de chave identifica o conteúdo protegido da perspectiva da licença. Embora você possa usar a mesma ID de chave para vários arquivos, é recomendável sempre usar uma ID de chave exclusiva para cada parte do conteúdo protegido.

Muitos dos métodos descritos nesta documentação usam cadeias de caracteres de ID de chave para selecionar licenças. Essas cadeias de caracteres contêm a ID da chave codificada em base64.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




