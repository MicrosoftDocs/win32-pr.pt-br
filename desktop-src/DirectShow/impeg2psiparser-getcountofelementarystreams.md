---
description: 'Método IMpeg2PsiParser:: GetCountOfElementaryStreams – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Método IMpeg2PsiParser:: GetCountOfElementaryStreams'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089154"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>Método IMpeg2PsiParser:: GetCountOfElementaryStreams

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

O `GetCountOfElementaryStreams` método recupera o número de fluxos elementares em um programa especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wProgramNumber* \[ no\]
</dt> <dd>

Especifica o \_ campo de número do programa para o programa, conforme fornecido no Pat.

</dd> <dt>

*pwVal* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o número de fluxos elementares no programa.

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

 

 




