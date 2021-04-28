---
description: 'Método IMpeg2PsiParser:: GetCountOfPrograms – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Método IMpeg2PsiParser:: GetCountOfPrograms'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119424"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Método IMpeg2PsiParser:: GetCountOfPrograms

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

O `GetCountOfPrograms` método recupera o número de programas no fluxo de transporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNumOfPrograms* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o número de programas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um valor HRESULT. Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Sucesso.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




