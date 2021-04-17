---
title: Método ClosedCaption. getSAMILangName
description: O método getSAMILangName recupera o nome de um idioma com suporte no arquivo SAMI atual.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- método getSAMILangName Windows Media Player
- método getSAMILangName Windows Media Player, classe ClosedCaption
- Classe ClosedCaption Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811342"
---
# <a name="closedcaptiongetsamilangname-method"></a>Método ClosedCaption. getSAMILangName

O método **getSAMILangName** recupera o nome de um idioma com suporte no arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) especificando o índice do nome do idioma a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres** que contém o nome do idioma, conforme especificado no arquivo Sami.

## <a name="remarks"></a>Comentários

Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

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

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





