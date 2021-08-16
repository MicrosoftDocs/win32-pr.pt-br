---
title: PLAYLIST. setColumnResizeMode
description: O método setColumnResizeMode especifica como os tamanhos de coluna indexados em si.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Windows Media Player de PLAYLIST. setColumnResizeMode
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335798"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST. setColumnResizeMode

O método **setColumnResizeMode** especifica como os tamanhos de coluna indexados em si.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*pilha*
</dt> <dd>

**Número** (**longo**) indicando o índice da coluna a ser alterada.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*moda*
</dt> <dd>

**Cadeia de caracteres** que indica o modo de dimensionamento. Contém um dos seguintes valores.



| Valor          | Descrição                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | A coluna é redimensionada para acomodar todos os dados na coluna e no cabeçalho.                                  |
| AutosizeData   | A coluna é redimensionada para acomodar todos os dados somente na coluna.                                                 |
| Fixo          | A coluna é um tamanho fixo.                                                                                    |
| Se estende      | A coluna é redimensionada para usar o espaço restante no elemento **playlist** depois que todas as outras colunas são redimensionadas. |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





