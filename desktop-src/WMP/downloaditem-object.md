---
title: Objeto DownloadItem
description: Objeto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Armazenamentos online do Windows Media Player, objeto DownloadItem
- lojas online, objeto DownloadItem
- tipo 2 lojas online, objeto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788177"
---
# <a name="downloaditem-object"></a>Objeto DownloadItem

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O objeto **DownloadItem** representa uma solicitação de download de arquivo. Ele pode ser usado por páginas da Web hospedadas no modo completo do Windows Media Player e que têm acesso ao objeto **externo** , como os serviços Premium.

O objeto **DownloadItem** dá suporte às propriedades a seguir.



| Propriedade                                        | Descrição                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadstate](downloaditem-downloadstate.md) | Recupera o estado do download.             |
| [andamento](downloaditem-progress.md)           | Recupera o progresso do download em bytes. |
| [size](downloaditem-size.md)                   | Recupera o tamanho do download.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera a URL de origem do download.        |
| [tipo](downloaditem-type.md)                   | Recupera o tipo de download.              |



 

O objeto **DownloadItem** dá suporte aos métodos a seguir.



| Método                                      | Descrição                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Cancela o download.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera o valor de um atributo para o item de download. |
| [pause](downloaditem-pause.md)             | Pausa o download.                                       |
| [Volte](downloaditem-resume.md)           | Retoma o download.                                      |



 

O objeto **DownloadItem** é acessado por meio da propriedade a seguir.



| Objeto                                              | Propriedade                            |
|-----------------------------------------------------|-------------------------------------|
| [Downloadcollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Para fins de ilustração, o **DownloadManager**. **Getbaixecollection**(*CollectionId*). **Item**(*ItemId*) é usado nas seções de sintaxe de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




