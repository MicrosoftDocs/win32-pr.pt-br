---
title: Objeto downloadcollection
description: Objeto downloadcollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Armazenamentos online do Windows Media Player, objeto Downloadcollection
- repositórios online, objeto Downloadcollection
- tipo 2 lojas online, objeto Downloadcollection
- Downloadcollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761468"
---
# <a name="downloadcollection-object"></a>Objeto downloadcollection

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O objeto **downloadcollection** contém propriedades e métodos para lidar com coleções de itens de download. Ele pode ser usado por páginas da Web hospedadas no modo completo do Windows Media Player e que têm acesso ao objeto **externo** , como lojas online.

O objeto **downloadcollection** dá suporte às propriedades a seguir.



| Propriedade                              | Descrição                                  |
|---------------------------------------|----------------------------------------------|
| [contagem](downloadcollection-count.md) | Recupera o número de downloads pendentes.   |
| [id](downloadcollection-id.md)       | Recupera a ID da coleção de download. |



 

O objeto **downloadcollection** dá suporte aos métodos a seguir.



| Método                                                | Descrição                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Limpar](downloadcollection-clear.md)                 | Remove todos os itens de uma coleção de download. |
| [item](downloadcollection-item.md)                   | Recupera um objeto de download pendente.          |
| [removeItem](downloadcollection-removeitem.md)       | Remove um item de download de uma coleção.    |
| [startDownload](downloadcollection-startdownload.md) | Enfileira um download.                            |



 

O objeto **downloadcollection** é acessado por meio dos métodos a seguir.



| Objeto                                        | Método                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createbaixecollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getbaixecollection](downloadmanager-getdownloadcollection.md)       |



 

Para fins de ilustração, o **DownloadManager**. **Getbaixecollection**(*CollectionId*) é usado nas seções de sintaxe de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




