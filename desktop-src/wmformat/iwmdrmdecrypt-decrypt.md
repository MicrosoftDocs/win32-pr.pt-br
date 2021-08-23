---
title: Método Decrypt IWMDRMDecrypt (Wmdrmsdk.h)
description: O método Decrypt descriptografa um buffer de dados no local.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Descriptografar o formato de mídia do windows do método
- Descriptografar o método Windows Media Format, interface IWMDRMDecrypt
- Formato de mídia da interface IWMDRMDecrypt, método Decrypt
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
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027743"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>Método IWMDRMDecrypt::D ecrypt

O **método Decrypt** descriptografa um buffer de dados no local.

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

*pbData* \[ in, out\]
</dt> <dd>

Dados a serem descriptografados. Se o método for bem-sucedido, esses dados serão descriptografados no retorno.

</dd> <dt>

*cbData* \[ Em\]
</dt> <dd>

Tamanho dos dados em bytes.

</dd> <dt>

*pWMCryptoData* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros extras. Pode ser **NULL** se o conteúdo foi criptografado usando os parâmetros padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDecrypt Interface**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





