---
description: O método GetTitleParentalLevels recupera os níveis de gerenciamento de pais para o título especificado.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Método GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ef462767c280f5e6f1c58679a78ee876e58042dce632f30711c198b4ca574a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536666"
---
# <a name="gettitleparentallevels-method"></a>Método GetTitleParentalLevels

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetTitleParentalLevels` método recupera os níveis de gerenciamento de pais para o título especificado.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o título como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro cujos bits individuais indicam quais níveis de gerenciamento de pais (PML) estão definidos no título especificado.

## <a name="remarks"></a>Comentários

Um título pode ter capítulos ou até mesmo segmentos curtos que têm um PML diferente do PML geral para o título. Use este método para determinar todos os PMLs que serão encontrados durante a reprodução de um título especificado. O número inteiro retornado é um conjunto de sinalizadores de bits definidos conforme mostrado na tabela a seguir. Execute uma operação AND bit a bit em *iLevels* e cada valor possível. Se a operação retornar **true**, isso significará que PML será encontrado em algum ponto deste título.



| Valor  | Descrição          |
|--------|----------------------|
| 0x100  | Nível pai do DVD 1 |
| 0x200  | Nível pai do DVD 2 |
| 0x400  | Nível pai do DVD 3 |
| 0x800  | Nível pai do DVD 4 |
| 0x1000 | Nível pai do DVD 5 |
| 0x2000 | Nível pai do DVD 6 |
| 0x4000 | Nível pai do DVD 7 |
| 0x8000 | Nível pai do DVD 8 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



