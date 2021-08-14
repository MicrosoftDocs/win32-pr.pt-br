---
description: Método IMpeg2PsiParser::GetCountOfPrograms – a implementação desse método é fornecida como código de exemplo com o SDK do DirectShow. Não é uma API de DirectShow com suporte.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: Método IMpeg2PsiParser::GetCountOfPrograms
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
ms.openlocfilehash: c0c5609f82db98caea02e08f1e4fbd3877eeccbae25a5e83da3ac2804577b100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398103"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Método IMpeg2PsiParser::GetCountOfPrograms

A implementação desse método é fornecida como código de exemplo com o DirectShow SDK. Não é uma API de DirectShow com suporte.

O `GetCountOfPrograms` método recupera o número de programas no fluxo de transporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNumOfPrograms* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o número de programas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um valor HRESULT. Os valores possíveis incluem, mas não estão limitados a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Description         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMpeg2PsiParser Interface**](impeg2psiparser.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




