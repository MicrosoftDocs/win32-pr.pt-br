---
description: Cria um objeto enumerador e passa de volta um ponteiro para sua interface IEnumWiaItem2 para pastas com itens na árvore IWiaItem2 de um dispositivo WIA (Aquisição de Imagem) 2.0 do Windows.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: Método IWiaItem2::EnumChildItems (Wia.h)
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
ms.openlocfilehash: 921a6b6e85f906ef62683038b2bb28dd484d58fd20600b2ff85ae594fafb3cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440414"
---
# <a name="iwiaitem2enumchilditems-method"></a>Método IWiaItem2::EnumChildItems

Cria um objeto enumerador e passa de volta um ponteiro para sua interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para pastas com itens na árvore [**IWiaItem2**](-wia-iwiaitem2.md) de um dispositivo WIA (Aquisição de Imagem) 2.0 do Windows.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCategoryGUID* \[ Em\]
</dt> <dd>

Tipo: **const \* GUID**

Especifica um ponteiro para uma categoria para a qual os nós filho são enumerados. Se **NULL**, todos os nós filho serão enumerados.

</dd> <dt>

*ppIEnumWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que esse método cria.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O sistema de tempo de run time do WIA 2.0 representa cada dispositivo de hardware WIA 2.0 como uma árvore hierárquica [**de objetos IWiaItem2.**](-wia-iwiaitem2.md) O **método IWiaItem2::EnumChildItems** permite que os aplicativos enumeram itens filho no item atual. No entanto, ele só pode ser aplicado a itens que são pastas.

Se a pasta não estiver vazia, ela conterá uma subárvore de [**objetos IWiaItem2.**](-wia-iwiaitem2.md) O **método IWiaItem2::EnumChildItems** enumera todos os itens contidos na pasta . Ele armazena um ponteiro para um enumerador no *parâmetro ppIEnumWiaItem2.* Os aplicativos usam o ponteiro do enumerador para executar a enumeração de itens filho de um objeto.

Os aplicativos devem chamar o método [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface que recebem por meio do *parâmetro ppIEnumWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
