---
title: Método IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: O método EncryptScatter desembaralha e criptografa os dados.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Formato de mídia do Windows do método EncryptScatter
- Método EncryptScatter Windows Media Format, interface IWMDRMEncryptScatter
- Formato de mídia do Windows de interface IWMDRMEncryptScatter, método EncryptScatter
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
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762808"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Método IWMDRMEncryptScatter:: EncryptScatter

O método **EncryptScatter** desembaralha e criptografa os dados.

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

*cBlocks* \[ no\]
</dt> <dd>

Número de elementos na matriz *rgBlocks* .

</dd> <dt>

*rgBlocks* \[ no\]
</dt> <dd>

Matriz de uma ou mais estruturas de [**\_ \_ \_ bloco de dispersão criptografadas WMDRM**](wmdrm-encrypt-scatter-block.md) . Cada elemento descreve um bloco de dados para serem codificados e criptografados.

</dd> <dt>

*pWMCryptoData* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros de criptografia. Defina como **nulo** para usar os parâmetros padrão.

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

Tamanho do buffer de dados de saída passado como *pbOutput*.

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

Buffer de saída.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Interface IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





