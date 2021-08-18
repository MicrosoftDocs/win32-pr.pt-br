---
description: As constantes LINELOCATIONOPTION definem valores usados no membro dwOptions da estrutura LINELOCATIONENTRY retornada como parte da estrutura LINETRANSLATECAPS retornada por \_ lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45de77a6d887b6fb0c5fa0e45e7005a621aa10ca44cc3218078eea74d00a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003044"
---
# <a name="linelocationoption_-constants"></a>Constantes LINELOCATIONOPTION \_

As **constantes LINELOCATIONOPTION \_** definem valores usados no membro **dwOptions** da estrutura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) retornada como parte da estrutura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) retornada por [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



O modo de discagem padrão nesse local é a discagem de pulso. Se esse bit estiver definido, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirá um modificador discado "P" no início da cadeia de caracteres discável retornada quando esse local for selecionado. Se esse bit não estiver definido, **lineTranslateAddress** inserirá um modificador de discagem "T" no início da cadeia de caracteres discável.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Não extensível. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




