---
title: Objeto DownloadItem
description: Objeto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player online, objeto DownloadItem
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
ms.openlocfilehash: 6bfea6241e81352b8848304c3601650ef4dec2a8e5692874fa20995ccddcce38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863456"
---
# <a name="downloaditem-object"></a>Objeto DownloadItem

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **objeto DownloadItem** representa uma solicitação de download de arquivo. Ele pode ser usado por páginas da Web hospedadas no modo completo Windows Media Player  e que têm acesso ao objeto Externo, como serviços premium.

O **objeto DownloadItem** dá suporte às propriedades a seguir.



| Propriedade                                        | Descrição                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Recupera o estado do download.             |
| [Progresso](downloaditem-progress.md)           | Recupera o progresso do download em bytes. |
| [size](downloaditem-size.md)                   | Recupera o tamanho do download.              |
| [sourceURL](downloaditem-sourceurl.md)         | Recupera a URL de origem do download.        |
| [tipo](downloaditem-type.md)                   | Recupera o tipo do download.              |



 

O **objeto DownloadItem** dá suporte aos métodos a seguir.



| Método                                      | Descrição                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Cancela o download.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Recupera o valor de um atributo para o item de download. |
| [pause](downloaditem-pause.md)             | Pausa o download.                                       |
| [Currículo](downloaditem-resume.md)           | Retoma o download.                                      |



 

O **objeto DownloadItem** é acessado por meio da propriedade a seguir.



| Objeto                                              | Propriedade                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

Para fins de ilustração, **DownloadManager**. **getDownloadCollection**(*collectionId*). **item**(*itemId*) é usado nas seções de sintaxe de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




