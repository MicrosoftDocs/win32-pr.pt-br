---
title: DownloadItem. Type
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade Type recupera o tipo de download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. digite Windows Media Player
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
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788176"
---
# <a name="downloaditemtype"></a>DownloadItem. Type

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **Type** recupera o tipo de download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que contém um dos valores a seguir.



| Valor      | Descrição                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Somente Windows XP.) O download ocorre como um processo em segundo plano à medida que o tempo do processador se torna disponível. Os Estados de download persistem mesmo quando o Windows Media Player ou o Windows XP é desligado. |
| em tempo real  | (Todos os sistemas operacionais com suporte.) O download ocorre de uma só vez. Nenhum estado de download persiste entre sessões.                                                                       |



 

## <a name="remarks"></a>Comentários

Cada tipo de download tem vantagens e desvantagens. O download em segundo plano permite que o usuário prossiga para outras tarefas e até mesmo reinicie o Windows sem cancelar o download, mas leva mais tempo em geral para concluir o download e só tem suporte para o Windows XP. O download em tempo real leva menos tempo para ser concluído, mas exige que o usuário Conclua todo o download antes de fechar o Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





