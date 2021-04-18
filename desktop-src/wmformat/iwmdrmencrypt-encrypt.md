---
title: Método Encrypt de IWMDRMEncrypt (wmdrmsdk. h)
description: O método Encrypt criptografa um buffer de dados no local.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Método Encrypt Windows Media Format
- Método Encrypt Windows Media Format, interface IWMDRMEncrypt
- Formato de mídia do Windows da interface IWMDRMEncrypt, método Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787756"
---
# <a name="iwmdrmencryptencrypt-method"></a>Método IWMDRMEncrypt:: Encrypt

O método **Encrypt** criptografa um buffer de dados no local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbData* \[ entrada, saída\]
</dt> <dd>

Dados a serem criptografados. Se o método tiver sucesso, os dados serão criptografados no retorno.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

Tamanho dos dados em bytes.

</dd> <dt>

*pWMCryptoData* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros extras. Defina como **nulo** para usar os valores de criptografia padrão.

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

[**Interface IWMDRMEncrypt**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





