---
description: As \_ constantes LINELOCATIONOPTION definem os valores usados no membro dwOptions da estrutura LINELOCATIONENTRY retornada como parte da estrutura LINETRANSLATECAPS retornada por lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Constantes de LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753536"
---
# <a name="linelocationoption_-constants"></a>\_Constantes LINELOCATIONOPTION

As **constantes \_ LINELOCATIONOPTION** definem os valores usados no membro **dwOptions** da estrutura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) retornada como parte da estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retornada por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



O modo de discagem padrão neste local é a discagem de pulso. Se esse bit for definido, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirá um modificador de discagem "P" no início da cadeia de caracteres de seqüência retornada quando esse local for selecionado. Se esse bit não estiver definido, **lineTranslateAddress** inserirá um modificador de discagem "T" no início da cadeia de caracteres de seqüência.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




