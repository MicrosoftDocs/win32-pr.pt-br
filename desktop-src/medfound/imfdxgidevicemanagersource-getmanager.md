---
description: Obtém o IMFDXGIDeviceManager do Microsoft Media Foundation de renderização de vídeo.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: Método IMFDXGIDeviceManagerSource::GetManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 9e42e42e88dfa2acec9061a54f3a8fcc96128ad5aee6ff004e49f6dd10062074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957826"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>Método IMFDXGIDeviceManagerSource::GetManager

Obtém [**o IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) do Microsoft Media Foundation de renderização de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

O [**objeto IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




