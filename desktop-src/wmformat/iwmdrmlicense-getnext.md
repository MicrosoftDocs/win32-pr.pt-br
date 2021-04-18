---
title: Método GetNext IWMDRMLicense (wmdrmsdk. h)
description: O método GetNext carrega as informações sobre o próximo item na lista.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Formato do Windows Media do método GetNext
- Método GetNext Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771550"
---
# <a name="iwmdrmlicensegetnext-method"></a>Método IWMDRMLicense:: GetNext

O método **GetNext** carrega as informações sobre o próximo item na lista.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**ERRO \_ não há \_ mais \_ itens**</dt> </dl>      | Não há mais itens na lista.<br/>          |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

Os métodos da interface [**IWMDRMLicense**](iwmdrmlicense.md) fornecem dados sobre uma única licença por vez. O objeto subjacente contém uma lista de uma ou mais licenças. Quando você chama esse método, a interface move suas referências internas para a próxima licença na lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





