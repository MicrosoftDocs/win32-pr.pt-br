---
title: Método ClosedCaption. getSAMILangID
description: O método getSAMILangID recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- Windows Media Player do método getSAMILangID
- método getSAMILangID Windows Media Player, classe ClosedCaption
- classe ClosedCaption Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7317bff13b0dcf29157e4a31c1b854fff781d93460633b64485670fab64e6f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764036"
---
# <a name="closedcaptiongetsamilangid-method"></a>Método ClosedCaption. getSAMILangID

O método **getSAMILangID** recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) ESPECIFICANDO o índice do LCID a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **número** (**Long**) que contém o LCID do idioma com o índice especificado.

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
</dt> </dl>

 

 





