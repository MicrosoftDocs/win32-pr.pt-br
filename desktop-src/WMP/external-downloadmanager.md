---
title: Externo. DownloadManager
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade DownloadManager recupera o objeto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Externo. DownloadManager Windows Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779999"
---
# <a name="externaldownloadmanager"></a>Externo. DownloadManager

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **DownloadManager** recupera o objeto **DownloadManager** .

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto **DownloadManager** somente leitura.

## <a name="remarks"></a>Comentários

No Windows Media Player 10 ou posterior, a propriedade e o objeto **DownloadManager** são acessíveis somente de painéis de tarefas do serviço de loja online. Você não pode usar o **DownloadManager** de outros recursos em que o objeto **externo** está disponível, como HtmlView, exibição do centro de informações e informações do álbum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





