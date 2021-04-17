---
description: A interface IKsPin fornece um método para recuperar os meios suportados por um PIN em um filtro de modo kernel. O IKsPin tem métodos adicionais além daquele mostrado aqui, mas eles não têm suporte para o DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interface IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759541"
---
# <a name="ikspin-interface"></a>Interface IKsPin

A `IKsPin` interface fornece um método para recuperar os meios suportados por um PIN em um filtro de modo kernel. `IKsPin` tem métodos adicionais além daquele mostrado aqui, mas eles não têm suporte para o DirectShow.

## <a name="members"></a>Membros

A interface **IKsPin** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPin** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IKsPin** tem esses métodos.



| Método                                          | Descrição                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera os meios com suporte por um PIN.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
