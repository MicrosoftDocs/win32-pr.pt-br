---
description: Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Método IItemPropertyBag:: GetPropertyInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762134"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Método IItemPropertyBag:: GetPropertyInfo

Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iProperty* \[ no\]
</dt> <dd>

O índice de base zero da primeira propriedade para a qual as informações são solicitadas.

</dd> <dt>

*cProperties* \[ no\]
</dt> <dd>

O número de propriedades para as quais obter informações. Esse argumento especifica o número de elementos de matriz em *pPropBag*.

</dd> <dt>

*pPropBag* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de estruturas do [**doprop**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recebe as informações para as propriedades.

</dd> <dt>

*pcProperties* \[ fora\]
</dt> <dd>

Recebe um ponteiro para uma variável **ULONG** que recebe o número de propriedades para as quais as informações foram recuperadas.

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

 

 




