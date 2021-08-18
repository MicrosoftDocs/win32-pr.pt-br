---
title: DownloadItem. downloadstate
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade downloadstate recupera o estado do download.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem. downloadstate Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f2f1d7338370aaa5132c479d155ffbfc4282a686d082df37446be053efab3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997046"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem. downloadstate

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **downloadstate** recupera o estado do download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura que contém um dos valores a seguir.



| Valor | Descrição |
|-------|-------------|
| 0     | Baixando |
| 1     | Em Pausa      |
| 2     | Processing  |
| 3     | Concluído   |
| 4     | Canceled    |



 

## <a name="remarks"></a>Comentários

Os Estados de download podem ocorrer em qualquer ordem. Não grave o código que depende da ocorrência de qualquer estado de download específico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





