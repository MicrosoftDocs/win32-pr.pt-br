---
title: DownloadCollection.id
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade id recupera a ID da coleção de download.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e505db2e643286f84b61bfa8604b9edc8ef36fa39cdd040bd9cc49bb98f82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651260"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade id** recupera a ID da coleção de download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Quando o Gerenciador de Download cria uma nova coleção de download, ele atribui à coleção um número de ID. Os números de ID persistem entre Windows Media Player sessões e sessões do sistema operacional.

Os números de ID não são exclusivos. No entanto, há números de ID suficientes disponíveis no valor de 32 bits que é extremamente improvável que um número de ID existente seja substituído por um novo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





