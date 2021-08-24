---
description: Método IMpeg2PsiParser::GetPatVersionNumber – a implementação desse método é fornecida como código de exemplo com o SDK do DirectShow. Não é uma API de DirectShow com suporte.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: Método IMpeg2PsiParser::GetPatVersionNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: ffd03bea09fb9041b91bb214287442eb59a7101be7a8841e0d38e28bcdaf3ecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767356"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Método IMpeg2PsiParser::GetPatVersionNumber

A implementação desse método é fornecida como código de exemplo com o DirectShow SDK. Não é uma API de DirectShow com suporte.

O `GetPatVersionNumber` método recupera o campo de número de versão do \_ PAT. Um fluxo de transporte contém no máximo um PAT. O número de versão é incrementado sempre que as informações na tabela são mudadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPatVersion* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o campo número \_ de versão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **valor HRESULT.** Os valores possíveis incluem, mas não estão limitados a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMpeg2PsiParser Interface**](impeg2psiparser.md)
</dt> <dt>

[Exemplo de filtro do analisador PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




