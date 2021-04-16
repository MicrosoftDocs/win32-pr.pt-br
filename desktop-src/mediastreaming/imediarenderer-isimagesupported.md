---
title: Método IMediaRenderer IsImageSupported
description: Recupera um valor que indica se o DMR é capaz de exibir imagens.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API de streaming de mídia do método IsImageSupported
- API de streaming de mídia do método IsImageSupported, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105772642"
---
# <a name="imediarendererisimagesupported-method"></a>Método IMediaRenderer:: IsImageSupported

Recupera um valor que indica se o DMR é capaz de exibir imagens.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que será **true** se o DMR for capaz de exibir imagens e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





