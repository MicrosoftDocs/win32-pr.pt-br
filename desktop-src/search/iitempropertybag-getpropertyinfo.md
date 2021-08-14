---
description: Obtém as informações necessárias para ler ou salvar as propriedades no pacote de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: Método IItemPropertyBag::GetPropertyInfo
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
ms.openlocfilehash: 7a69ceff2236a101f18ee06b4a87dd60e35ca69e73fdeb085232f102f8450d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863085"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Método IItemPropertyBag::GetPropertyInfo

Obtém as informações necessárias para ler ou salvar as propriedades no pacote de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

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

*iProperty* \[ Em\]
</dt> <dd>

O índice baseado em zero da primeira propriedade para a qual as informações são solicitadas.

</dd> <dt>

*cProperties* \[ Em\]
</dt> <dd>

O número de propriedades para as que obter informações. Esse argumento especifica o número de elementos de matriz em *pPropBag.*

</dd> <dt>

*pPropBag* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recebe as informações das propriedades.

</dd> <dt>

*pcProperties* \[ out\]
</dt> <dd>

Recebe um ponteiro para uma **variável ULONG** que recebe o número de propriedades para as quais as informações foram recuperadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

Para visualizar anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPropertyBag**](iitempropertybag.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) as estruturas [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 3.0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




