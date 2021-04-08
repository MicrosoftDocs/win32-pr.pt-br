---
title: Método IMsRdpDeviceCollection2 RedirectNow
description: Força os dispositivos que foram selecionados ou desmarcados da coleção a serem redirecionados ou removidos.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RedirectNow
- Método RedirectNow Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection2, método RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918002"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>Método IMsRdpDeviceCollection2:: RedirectNow

Força os dispositivos que foram selecionados ou desmarcados da coleção a serem redirecionados ou removidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Um valor da enumeração [**RedirectDeviceType**](redirectdevicetype.md) que especifica o tipo de dispositivo a ser redirecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





