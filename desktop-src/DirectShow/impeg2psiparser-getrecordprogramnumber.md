---
description: 'Método IMpeg2PsiParser:: GetRecordProgramNumber – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
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
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089134"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Método IMpeg2PsiParser:: GetRecordProgramNumber

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

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
| <dl> <dt>**S \_ OK**</dt> </dl> | Sucesso.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




