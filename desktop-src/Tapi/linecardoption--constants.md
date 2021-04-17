---
description: As \_ constantes LINECARDOPTION definem os valores usados no membro dwOptions da estrutura LINECARDENTRY retornada como parte da estrutura LINETRANSLATECAPS retornada por lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Constantes de LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754734"
---
# <a name="linecardoption_-constants"></a>\_Constantes LINECARDOPTION

As **\_ constantes LINECARDOPTION** definem os valores usados no membro **dwOptions** da estrutura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) retornada como parte da estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retornada por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps). As **\_ constantes LINECARDOPTION** t têm os seguintes valores:

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ oculto**
</dt> <dd> <dl> <dt>



Este cartão de chamada foi ocultado pelo usuário. Ele não é mostrado pelo auxiliar de discagem na lista principal de cartões de chamada disponíveis, mas será mostrado na lista de cartões dos quais as regras de discagem podem ser copiadas.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ predefinido**
</dt> <dd> <dl> <dt>



Esse cartão de chamada é uma das definições de cartão de chamada predefinidas incluídas com a telefonia pela Microsoft. Ele não pode ser removido totalmente usando o auxiliar de discagem; Se o usuário tentar removê-lo, ele ficará oculto. Portanto, ele continua acessível para cópia de regras de discagem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




