---
title: Chave e ID da chave
description: Chave e ID da chave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), chaves
- DRM (gerenciamento de direitos digitais), criança
- DRM (gerenciamento de direitos digitais), KID
- ID da chave (KID)
- KID (ID da chave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765664"
---
# <a name="key-and-key-id"></a>Chave e ID da chave

Ao empacotar um arquivo, você usa uma chave. Uma chave é uma parte dos dados usados nos algoritmos de criptografia que protegem o conteúdo. Há duas partes para cada chave: uma semente de chave de licença e uma ID de chave (muitas vezes abreviadas como KID). A ID da chave é pública e é armazenada no cabeçalho do arquivo como uma maneira de identificar a chave necessária para descriptografar o arquivo. A semente da chave de licença é um valor secreto que deve ser compartilhado pelo empacotador de conteúdo e pelo emissor da licença.

Uma ID de chave identifica o conteúdo protegido da perspectiva da licença. Embora você possa usar a mesma ID de chave para vários arquivos, é recomendável usar sempre uma ID de chave exclusiva para cada parte do conteúdo protegido.

Muitos dos métodos descritos nesta documentação usam cadeias de caracteres de ID de chave para selecionar licenças. Essas cadeias de caracteres contêm a ID de chave codificada em base64.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




