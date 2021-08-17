---
description: Encerra o experiement e conclui o log de gráficos.
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine2:: endexperimento'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72c3893e3cadff355fd3d082b119a3a86d483c706265f66b90a26e56b371bc2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456946"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>Método IPixEngine2:: endexperimento

Encerra o experiement e conclui o log de gráficos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a>Parâmetros

*Restaura*   
Uma cadeia de caracteres COM que contém o nome do log de gráficos.

*pCallback*   
O endereço de um retorno de chamada usado para indicar que o experiement foi finalizado.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
