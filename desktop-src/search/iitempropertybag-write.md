---
description: Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Método IItemPropertyBag:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090050"
---
# <a name="iitempropertybagwrite-method"></a>Método IItemPropertyBag:: Write

Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cProperties* \[ no\]
</dt> <dd>

O número de propriedades a serem salvas. Esse argumento especifica o número de elementos nas matrizes em *pPropBag* e *pvarValue*.

</dd> <dt>

*pPropBag* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades a serem salvas.

</dd> <dt>

*pvarValue* \[ no\]
</dt> <dd>

Ponteiro para uma **variante** cujo tipo depende do tipo de dados das informações de propriedade que ela contém.

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

 

 




