---
description: Recupera o tipo de relação que esse IContextLink representa.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Método IContextLink:: GetContextLinkDirection (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164550"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a>Método IContextLink:: GetContextLinkDirection

Recupera o tipo de relação que esse [**IContextLink**](icontextlink.md) representa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextLinkDirection* \[ fora\]
</dt> <dd>

A direção que esse [**IContextLink**](icontextlink.md) representa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




