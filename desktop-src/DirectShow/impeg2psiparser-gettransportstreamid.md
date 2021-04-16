---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Método IMpeg2PsiParser:: GetTransportStreamId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754243"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>Método IMpeg2PsiParser:: GetTransportStreamId

A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.

O `GetTransportStreamId` método recupera o \_ \_ campo ID do fluxo de transporte do Pat. Esse valor é definido pelo usuário e pode ser usado para distinguir um fluxo de transporte específico de outros fluxos na mesma rede. Um fluxo de transporte contém no máximo uma PAT.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStreamId* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o \_ campo ID do fluxo de transporte \_ .

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

 

 




