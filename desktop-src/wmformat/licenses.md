---
title: Licenças
description: Licenças
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292766"
---
# <a name="licenses"></a>Licenças

Uma licença é um conjunto de dados que descreve as condições sob as quais os dados nos arquivos protegidos podem ser lidos. Cada licença se aplica a um identificador de chave, que normalmente é atribuído a um único arquivo de mídia. Esse identificador é usado para identificar o conteúdo protegido na licença.

Cada licença especifica uma ou mais ações que podem ser executadas com o conteúdo protegido. Essas ações, também chamadas de direitos, podem ser limitadas de várias maneiras. Ao combinar datas de início, datas de término, contagens e limites de tempo, o emissor da licença pode criar quase qualquer limitação imaginar à direita.

As licenças são emitidas por um serviço Web. Quando uma licença é adquirida, ela é armazenada no computador cliente no armazenamento de licença local, que é um arquivo protegido que contém licenças e outros dados de DRM. Quando o conteúdo protegido é acessado por um aplicativo, o subsistema DRM pesquisa o repositório de licenças local para uma licença que concede o direito apropriado. Se nenhuma licença for encontrada, o aplicativo poderá adquirir uma com base nas informações armazenadas no cabeçalho DRM do arquivo.

Várias licenças podem ser emitidas para o mesmo arquivo protegido. Quando o subsistema DRM determina se uma ação é permitida, ele agrega os direitos de todas as licenças que se aplicam. Cada licença pode ser atribuída a uma prioridade. Se mais de uma licença se aplicar a uma ação, a licença de prioridade mais alta será verificada para determinar se as contagens precisam ser decrementadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




