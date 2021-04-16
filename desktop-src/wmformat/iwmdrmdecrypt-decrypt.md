---
title: Método Decrypt IWMDRMDecrypt (wmdrmsdk. h)
description: O método Decrypt descriptografa um buffer de dados no local.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Método Decrypt Windows Media Format
- Método Decrypt Windows Media Format, interface IWMDRMDecrypt
- IWMDRMDecrypt interface formato Windows Media, método Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765076"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt: método ecrypt de:D

O método **Decrypt** descriptografa um buffer de dados no local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbData* \[ entrada, saída\]
</dt> <dd>

Dados a serem descriptografados. Se o método tiver sucesso, esses dados serão descriptografados no retorno.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

Tamanho dos dados em bytes.

</dd> <dt>

*pWMCryptoData* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros extras. Pode ser **NULL** se o conteúdo foi criptografado usando os parâmetros padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMDecrypt**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





