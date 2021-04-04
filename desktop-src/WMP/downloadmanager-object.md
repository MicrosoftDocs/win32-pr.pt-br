---
title: Objeto DownloadManager
description: Objeto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Armazenamentos online do Windows Media Player, objeto DownloadManager
- repositórios online, objeto DownloadManager
- tipo 2 lojas online, objeto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822733"
---
# <a name="downloadmanager-object"></a>Objeto DownloadManager

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O objeto **DownloadManager** é o objeto raiz do Gerenciador de download do Windows Media Player. Ele pode ser usado por páginas da Web hospedadas nos painéis de tarefas do serviço de loja online.

O objeto **DownloadManager** dá suporte aos métodos a seguir.



| Método                                                                   | Descrição                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createbaixecollection](downloadmanager-createdownloadcollection.md) | Cria uma coleção de download vazia.        |
| [getbaixecollection](downloadmanager-getdownloadcollection.md)       | Recupera a coleção de download especificada. |



 

O objeto **DownloadManager** é acessado usando **external. DownloadManager**. Para fins de ilustração, supõe-se que esse valor tenha sido atribuído a uma variável chamada "DownloadManager", que será usada para identificar esse objeto nas seções de sintaxe de referência.

No Windows Media Player 10 ou posterior, a propriedade e o objeto **DownloadManager** são acessíveis somente de painéis de tarefas do serviço de loja online. Você não pode usar o **DownloadManager** de outros recursos em que o objeto **externo** está disponível, como HtmlView, exibição do centro de informações e informações do álbum.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




