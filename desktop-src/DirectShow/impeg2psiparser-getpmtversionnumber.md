---
description: 'Método IMpeg2PsiParser:: GetPmtVersionNumber – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Método IMpeg2PsiParser:: GetPmtVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084554"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>Método IMpeg2PsiParser:: GetPmtVersionNumber

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

O `GetPmtVersionNumber` método recupera o \_ campo de número de versão de um PGTO especificado. O número de versão é incrementado sempre que a definição do programa é alterada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wProgramNumber* \[ no\]
</dt> <dd>

Especifica o \_ campo de número do programa do programa, conforme fornecido no Pat.

</dd> <dt>

*pPmtVersion* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o campo de número de versão \_ .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um valor **HRESULT** . Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Sucesso.<br/> |



 

## <a name="remarks"></a>Comentários

Use o método **GetRecordProgramNumber** para obter o número do programa.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




