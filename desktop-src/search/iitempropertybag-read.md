---
description: Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Método IItemPropertyBag:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296237"
---
# <a name="iitempropertybagread-method"></a>Método IItemPropertyBag:: Read

Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cProperties* \[ no\]
</dt> <dd>

O número de propriedades a serem lidas. Esse argumento especifica o número de elementos nas matrizes em *pPropBag*, *pvarValue* e *phrError*.

</dd> <dt>

*pPropBag* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades que são solicitadas.

</dd> <dt>

*pvarValue* \[ fora\]
</dt> <dd>

Recebe um ponteiro que retorna uma matriz de estruturas **Variant** que recebe os valores de propriedade.

</dd> <dt>

*phrError* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de valores **HRESULT** que recebe o resultado de cada propriedade lida. Deve haver pelo menos elementos *cProperties* nesta matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPropertyBag**](iitempropertybag.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




