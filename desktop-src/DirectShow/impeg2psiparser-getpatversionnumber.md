---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Método IMpeg2PsiParser:: GetPatVersionNumber'
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
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370115"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Método IMpeg2PsiParser:: GetPatVersionNumber

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

O `GetPatVersionNumber` método recupera o \_ campo de número de versão do Pat. Um fluxo de transporte contém no máximo uma PAT. O número de versão é incrementado sempre que as informações na tabela são alteradas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPatVersion* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o campo de número de versão \_ .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




