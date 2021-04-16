---
description: Cria um objeto de enumerador e retorna um ponteiro para sua interface IEnumWiaItem2 para pastas com itens na árvore IWiaItem2 de um dispositivo WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Método IWiaItem2:: EnumChildItems (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461146"
---
# <a name="iwiaitem2enumchilditems-method"></a>Método IWiaItem2:: EnumChildItems

Cria um objeto de enumerador e retorna um ponteiro para sua interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para pastas com itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) de um dispositivo WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCategoryGUID* \[ no\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica um ponteiro para uma categoria para a qual nós filhos são enumerados. Se _ * NULL * *, todos os nós filho serão enumerados.

</dd> <dt>

*ppIEnumWiaItem2* \[ fora\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que esse método cria.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O sistema de tempo de execução WIA 2,0 representa cada dispositivo de hardware WIA 2,0 como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . O método **IWiaItem2:: EnumChildItems** permite que os aplicativos enumerem itens filho no item atual. No entanto, ele só pode ser aplicado a itens que são pastas.

Se a pasta não estiver vazia, ela conterá uma subárvore de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . O método **IWiaItem2:: EnumChildItems** enumera todos os itens contidos na pasta. Ele armazena um ponteiro para um enumerador no parâmetro *ppIEnumWiaItem2* . Os aplicativos usam o ponteiro do enumerador para executar a enumeração dos itens filho de um objeto.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnumWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
