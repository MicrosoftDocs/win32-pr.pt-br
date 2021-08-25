---
title: Objeto DownloadCollection
description: Objeto DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player online, objeto DownloadCollection
- online stores,objeto DownloadCollection
- tipo 2 lojas online, objeto DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902016"
---
# <a name="downloadcollection-object"></a>Objeto DownloadCollection

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **objeto DownloadCollection** contém propriedades e métodos para lidar com coleções de itens de download. Ele pode ser usado por páginas da Web hospedadas no modo completo Windows Media Player  e que têm acesso ao objeto Externo, como lojas online.

O **objeto DownloadCollection** dá suporte às propriedades a seguir.



| Propriedade                              | Descrição                                  |
|---------------------------------------|----------------------------------------------|
| [contagem](downloadcollection-count.md) | Recupera o número de downloads pendentes.   |
| [id](downloadcollection-id.md)       | Recupera a ID da coleção de download. |



 

O **objeto DownloadCollection** dá suporte aos métodos a seguir.



| Método                                                | Descrição                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Limpar](downloadcollection-clear.md)                 | Remove todos os itens de uma coleção de download. |
| [item](downloadcollection-item.md)                   | Recupera um objeto de download pendente.          |
| [Removeitem](downloadcollection-removeitem.md)       | Remove um item de download de uma coleção.    |
| [startDownload](downloadcollection-startdownload.md) | Enfile um download.                            |



 

O **objeto DownloadCollection** é acessado por meio dos métodos a seguir.



| Objeto                                        | Método                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

Para fins de ilustração, **DownloadManager**. **getDownloadCollection**(*collectionId*) é usado nas seções de sintaxe de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




