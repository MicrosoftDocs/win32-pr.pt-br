---
title: DownloadItem.type
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade type recupera o tipo do download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem.type Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038f348093a512095ee930c4147024bc789ead5edd3498243eb83a01608bfac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749707"
---
# <a name="downloaditemtype"></a>DownloadItem.type

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade** type recupera o tipo do download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de **caracteres** somente leitura que contém um dos valores a seguir.



| Valor      | Descrição                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP somente.) O download ocorre como um processo em segundo plano à medida que o tempo do processador fica disponível. Os estados de download persistem mesmo quando Windows Media Player ou Windows XP é desligado. |
| em tempo real  | (Todos os sistemas operacionais com suporte.) O download ocorre de uma só vez. Nenhum estado de download persiste entre as sessões.                                                                       |



 

## <a name="remarks"></a>Comentários

Cada tipo de download tem vantagens e desvantagens. O download em segundo plano permite que o usuário prossiga para outras tarefas e até mesmo reinicie o Windows sem cancelar o download, mas leva mais tempo geral para concluir o download e só tem suporte para o Windows XP. O download em tempo real leva menos tempo para ser concluído, mas exige que o usuário conclua todos os downloads antes de fechar Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





