---
title: Sintaxe de intervalo
description: Representa um valor de intervalo de tempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Esquema do AD de sintaxe de intervalo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e088c8347ff12172cb87c521e049e2646a0711e1eaedf805887b6988af1e284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580286"
---
# <a name="interval-syntax"></a>Sintaxe de intervalo

Representa um valor de intervalo de tempo. As unidades de tempo reais dependem de qual atributo está usando essa sintaxe. Essa sintaxe é idêntica à sintaxe [**LargeInteger,**](s-largeinteger.md) exceto que os valores alto e baixo são inteiros sem sinal.



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Intervalo                                                                           |
| ID da sintaxe    | 2.5.5.16                                                                           |
| OM ID        | 65                                                                                 |
| Tipo MAPI    | \-                                                                                 |
| Tipo ADS     | ADSTYPE \_ INTEIRO \_ GRANDE                                                            |
| Tipo de variante | DISPATCH \_ da VT                                                                       |
| Tipo de SDS     | Um objeto COM que pode ser lançado em [**um IADsLargeInteger.**](/windows/desktop/api/iads/nn-iads-iadslargeinteger) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Iadslargeinteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
