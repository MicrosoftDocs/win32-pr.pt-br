---
description: Faz com que uma ou mais propriedades sejam lidas do pacote de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: Método IItemPropertyBag::Read
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
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226601"
---
# <a name="iitempropertybagread-method"></a>Método IItemPropertyBag::Read

Faz com que uma ou mais propriedades sejam lidas do pacote de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

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

*cProperties* \[ Em\]
</dt> <dd>

O número de propriedades a ler. Esse argumento especifica o número de elementos nas matrizes em *pPropBag,* *pvarValue* e *phrError.*

</dd> <dt>

*pPropBag* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades solicitadas.

</dd> <dt>

*pvarValue* \[ out\]
</dt> <dd>

Recebe um ponteiro que retorna uma matriz de estruturas **VARIANT** que recebe os valores de propriedade.

</dd> <dt>

*phrError* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de **valores HRESULT** que recebe o resultado de cada propriedade lida. Deve haver pelo menos *elementos cProperties* nessa matriz.

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

 

 




