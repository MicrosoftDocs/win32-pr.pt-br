---
title: Método ClosedCaption. getSAMIStyleName
description: O método getSAMIStyleName recupera o nome de um estilo com suporte no arquivo SAMI atual.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- método getSAMIStyleName Windows Media Player
- método getSAMIStyleName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813372"
---
# <a name="closedcaptiongetsamistylename-method"></a>Método ClosedCaption. getSAMIStyleName

O método **getSAMIStyleName** recupera o nome de um estilo com suporte no arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) especificando o índice do nome do estilo a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** que contém o nome do estilo, conforme especificado no arquivo Sami.

## <a name="remarks"></a>Comentários

Os estilos em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption. SAMIstyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





