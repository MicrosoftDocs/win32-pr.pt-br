---
title: Método IWMDRMLicense inclusionlist (wmdrmsdk. h)
description: O método getinclusõeslist recupera toda a lista de inclusão para a licença ou cadeia de licença atual.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Método inclusionlist formato de mídia do Windows
- Método getinclusõeslist Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método getinclusõeslist
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797921"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>Método IWMDRMLicense:: inclusionlist

O método **Getinclusõeslist** recupera toda a lista de inclusão para a licença ou cadeia de licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppGuids* \[ fora\]
</dt> <dd>

Recebe uma matriz de GUIDs que identifica as tecnologias incluídas.

</dd> <dt>

*pcGuids* \[ fora\]
</dt> <dd>

Recebe o número de elementos na matriz *ppGuids* . A matriz é alocada usando **CoTaskMemAlloc**. Quando terminar com a lista, libere a memória chamando **CoTaskMemFree**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O emissor da licença pode especificar outros sistemas de proteção para os quais o conteúdo criptografado pode ser convertido. A lista de GUIDs recuperados por esse método identifica os sistemas de proteção permitidos. Ao entrar em um contrato de licença com a Microsoft para obter a biblioteca de stub, você receberá uma lista de sistemas de proteção com suporte no momento e os GUIDs usados para identificá-los.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Autorização explícita e listas de inclusão**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





