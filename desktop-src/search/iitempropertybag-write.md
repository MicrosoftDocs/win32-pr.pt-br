---
description: Faz com que uma ou mais propriedades sejam salvas no pacote de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: Método IItemPropertyBag::Write
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
ms.openlocfilehash: e8860653244cef53739c7d104405a176c1ec63d2de1d3434b1d25e3206c431aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863105"
---
# <a name="iitempropertybagwrite-method"></a>Método IItemPropertyBag::Write

Faz com que uma ou mais propriedades sejam salvas no pacote de propriedades. A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e Windows Server 2003 e não deve mais ser usada.

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

*cProperties* \[ Em\]
</dt> <dd>

O número de propriedades a salvar. Esse argumento especifica o número de elementos nas matrizes em *pPropBag* e *pvarValue*.

</dd> <dt>

*pPropBag* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades a serem salvas.

</dd> <dt>

*pvarValue* \[ Em\]
</dt> <dd>

Ponteiro para uma **VARIANT** cujo tipo depende do tipo de dados das informações de propriedade que ele contém.

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

 

 




