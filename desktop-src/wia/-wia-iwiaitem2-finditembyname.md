---
description: Pesquisa a árvore de subitens de um item usando o nome como a chave de pesquisa.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'Método IWiaItem2:: FindItemByName (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772552"
---
# <a name="iwiaitem2finditembyname-method"></a>Método IWiaItem2:: FindItemByName

Pesquisa a árvore de subitens de um item usando o nome como a chave de pesquisa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrFullItemName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do item a ser pesquisado.

</dd> <dt>

*ppIWiaItem2* \[ fora\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item encontrado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método pesquisa a árvore do item atual de subitens usando o nome como a chave de pesquisa. Se **IWiaItem2:: FindItemByName** encontrar o item especificado por *bstrFullItemName*, ele armazenará o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item no parâmetro *ppIWiaItem2* .

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
