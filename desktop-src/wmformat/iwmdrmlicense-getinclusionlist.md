---
title: Método GetInclusionList de IWMDRMLicense (Wmdrmsdk.h)
description: O método GetInclusionList recupera toda a lista de inclusão para a cadeia de licenças ou licenças atual.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Formato de mídia do windows do método GetInclusionList
- Formato de mídia do método GetInclusionList , interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense , método GetInclusionList
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
ms.openlocfilehash: 6389ac30d5bffeb6ad354ec6c7e83f2834921fe8fb83c1abe2bca2d0c2f43bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705236"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>Método IWMDRMLicense::GetInclusionList

O **método GetInclusionList** recupera toda a lista de inclusão para a cadeia de licenças ou licenças atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Recebe uma matriz de GUIDs que identificam as tecnologias incluídas.

</dd> <dt>

*pcGuids* \[ out\]
</dt> <dd>

Recebe o número de elementos na *matriz ppGuids.* A matriz é alocada usando **CoTaskMemAlloc.** Quando terminar a lista, libere a memória chamando **CoTaskMemFree.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O emissor da licença pode especificar outros sistemas de proteção nos quais o conteúdo criptografado pode ser convertido. A lista de GUIDs recuperados por esse método identifica os sistemas de proteção permitidos. Ao entrar em um contrato de licença com a Microsoft para obter a biblioteca de stub, você receberá uma lista de sistemas de proteção com suporte no momento e os GUIDs usados para identificá-los.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Listas explícitas de autorização e inclusão**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





