---
description: Crie um novo item filho. Adiciona objetos IWiaItem2 à árvore IWiaItem2 do dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Método IWiaItem2:: createchilditem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965565"
---
# <a name="iwiaitem2createchilditem-method"></a>Método IWiaItem2:: createchilditem

Crie um novo item filho. Adiciona objetos [**IWiaItem2**](-wia-iwiaitem2.md) à árvore **IWiaItem2** do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lItemFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica o tipo de item WIA 2,0. Consulte [**sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lCreationFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica como criar o novo item.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Defina os valores padrão para as propriedades do filho.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copiar \_ \_ \_ Valores de propriedade pai** (0x40000000)


</dt> <dd>

Copie os valores de todas as propriedades de leitura/gravação do pai.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do item. Esse nome é acrescentado ao final do nome do item pai para gerar o nome completo do item.

</dd> <dt>

*ppIWiaItem2* \[ fora\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) que define o método **IWiaItem2:: createchilditem** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Alguns dispositivos de hardware WIA 2,0 permitem que os aplicativos criem novos itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) que representa o dispositivo. Os aplicativos devem testar os dispositivos para ver se eles dão suporte a esse recurso. Use a \_ interface IEnumWIA dev \_ Caps para enumerar os recursos atuais do dispositivo.

Se o dispositivo permitir a criação de novos itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) , invocar **IWiaItem2:: createchilditem** cria um novo objeto **IWiaItem2** que é filho do nó atual. Ele passa um ponteiro para o novo nó para o aplicativo por meio do parâmetro *ppIWiaItem2* . Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .

Se *lCreationFlags* for copiar \_ \_ \_ valores de propriedade pai e *lItemFlags* for zero, a função retornará E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
