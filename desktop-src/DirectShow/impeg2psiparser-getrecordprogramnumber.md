---
description: 'método IMpeg2PsiParser:: GetRecordProgramNumber – a implementação desse método é fornecida como um código de exemplo com o SDK DirectShow. não é uma API DirectShow com suporte.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Método IMpeg2PsiParser:: GetRecordProgramNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083696"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Método IMpeg2PsiParser:: GetRecordProgramNumber

a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. não é uma API DirectShow com suporte.

O `GetRecordProgramNumber` método recupera o número do programa para um programa especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Especifica a entrada no PAT que define o programa, indexado de zero.

</dd> <dt>

*pwVal* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o \_ campo de número do programa do Pat.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um valor **HRESULT** . Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




