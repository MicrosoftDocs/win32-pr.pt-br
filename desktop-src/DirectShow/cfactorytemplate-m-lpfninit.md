---
description: Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL. Pode ser NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Membro CFactoryTemplate:: m_lpfnInit (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750659"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Membro de CFactoryTemplate:: m \_ lpfnInit

Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL. Pode ser **NULL**.

## <a name="syntax"></a>Sintaxe


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Comentários

O tipo de ponteiro de função é [**LPFNInitRoutine**](lpfninitroutine.md). Se você fornecer essa função em sua DLL, a função de ponto de entrada de DLL a chamará com os seguintes parâmetros:

-   *bLoading*: **true** quando a dll é carregada, **false** quando a dll é descarregada.
-   *rclsid*: ponteiro para o CLISD do objeto, especificado na variável de membro [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




