---
description: Método IMpeg2PsiParser::GetTransportStreamId – a implementação desse método é fornecida como código de exemplo com o SDK do DirectShow. Não é uma API de DirectShow com suporte.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: Método IMpeg2PsiParser::GetTransportStreamId
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
ms.openlocfilehash: e78eabce23633029e4ef3dfe6c6777c586a5d74ed28ccfe466c89064851f8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791896"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>Método IMpeg2PsiParser::GetTransportStreamId

A implementação desse método é fornecida como código de exemplo com o DirectShow SDK. Não é uma API de DirectShow com suporte.

O `GetTransportStreamId` método recupera o campo de \_ \_ ID do fluxo de transporte do PAT. Esse valor é definido pelo usuário e pode ser usado para distinguir um fluxo de transporte específico de outros fluxos na mesma rede. Um fluxo de transporte contém no máximo um PAT.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStreamId* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o campo de \_ ID do \_ fluxo de transporte.

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

 

 




