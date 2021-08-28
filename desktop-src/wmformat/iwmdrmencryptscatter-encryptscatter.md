---
title: Método EncryptScatter IWMDRMEncryptScatter (Wmdrmsdk.h)
description: O método EncryptScatter desembrave e criptografa dados.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Formato de mídia do windows do método EncryptScatter
- Formato de mídia do windows do método EncryptScatter, interface IWMDRMEncryptScatter
- Formato de mídia da interface IWMDRMEncryptScatter , método EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fae3f8a40bc5468898424dcf33bf947235a632db44f4dada7f2c96b2a3a064b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839706"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Método IWMDRMEncryptScatter::EncryptScatter

O **método EncryptScatter** desembrave e criptografa dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cBlocks* \[ Em\]
</dt> <dd>

Número de elementos na matriz *rgBlocks.*

</dd> <dt>

*rgBlocks* \[ Em\]
</dt> <dd>

Matriz de uma ou mais [**estruturas WMDRM \_ ENCRYPT SCATTER \_ \_ BLOCK.**](wmdrm-encrypt-scatter-block.md) Cada elemento descreve um bloco de dados a serem não criptografados e criptografados.

</dd> <dt>

*pWMCryptoData* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros de criptografia. De definido **como NULL** para usar os parâmetros padrão.

</dd> <dt>

*cbOutput* \[ Em\]
</dt> <dd>

Tamanho do buffer de dados de saída passado como *pbOutput.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Buffer de saída.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter Interface**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





