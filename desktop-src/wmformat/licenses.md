---
title: Licenças
description: Licenças
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows SDK de Formato de Mídia, DRM (gerenciamento de direitos digitais)
- Windows SDK de Formato de Mídia, licenças DRM
- Windows SDK de Formato de Mídia, licenças para DRM
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b899e44ffdff5d2a7f3c5fb3237b477ae0143327a331f63bd9717e3ae4320483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700830"
---
# <a name="licenses"></a>Licenças

Uma licença é um conjunto de dados que descreve as condições sob as quais os dados em arquivos protegidos podem ser lidos. Cada licença se aplica a um identificador de chave, que normalmente é atribuído a um único arquivo de mídia. Esse identificador é o que é usado para identificar o conteúdo protegido na licença.

Cada licença especifica uma ou mais ações que podem ser executadas com o conteúdo protegido. Essas ações, também chamadas de direitos, podem ser limitadas de várias maneiras. Combinando datas de início, datas de término, contagens e limites de tempo, o emissor da licença pode criar quase qualquer limitação possível de um direito.

As licenças são emitidas por um serviço Web. Quando uma licença é adquirida, ela é armazenada no computador cliente no armazenamento de licenças local, que é um arquivo protegido que contém licenças e outros dados drm. Quando o conteúdo protegido é acessado por um aplicativo, o subsistema DRM pesquisa no armazenamento de licenças local uma licença que concede o direito apropriado. Se nenhuma licença for encontrada, o aplicativo poderá adquirir uma com base nas informações armazenadas no header drm do arquivo.

Várias licenças podem ser emitidas para o mesmo arquivo protegido. Quando o subsistema DRM determina se uma ação é permitida, ela agrega os direitos de todas as licenças que se aplicam. Cada licença pode ser atribuída a uma prioridade. Se mais de uma licença se aplicar a uma ação, a licença de prioridade mais alta será verificada para determinar se as contagens precisam ser decrementados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




