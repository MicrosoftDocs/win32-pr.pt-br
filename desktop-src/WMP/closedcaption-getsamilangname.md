---
title: Método ClosedCaption.getSAMILangName
description: O método getSAMILangName recupera o nome de um idioma com suporte no arquivo SAMI atual.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- Método getSAMILangName Windows Media Player
- Método getSAMILangName Windows Media Player , classe ClosedCaption
- Classe ClosedCaption Windows Media Player método , getSAMILangName
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
ms.openlocfilehash: a8d4150289eb7637d1772443a5437c6d245993ea0825a37d11bd7ec5accae918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764026"
---
# <a name="closedcaptiongetsamilangname-method"></a>Método ClosedCaption.getSAMILangName

O **método getSAMILangName** recupera o nome de um idioma com suporte no arquivo SAMI atual.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice do nome do idioma a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma **Cadeia de** caracteres que contém o nome do idioma, conforme especificado no arquivo SAMI.

## <a name="remarks"></a>Comentários

Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

Esse método não pode ser usado até que um arquivo de mídia digital seja aberto (*Player*.**openState** é igual a 13).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 





