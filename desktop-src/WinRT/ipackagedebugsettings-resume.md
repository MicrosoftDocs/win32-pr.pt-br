---
description: Retoma os processos do pacote se eles estiverem suspensos no momento.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Método IPackageDebugSettings:: resume'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807960"
---
# <a name="ipackagedebugsettingsresume-method"></a>Método IPackageDebugSettings:: resume

Retoma os processos do pacote se eles estiverem suspensos no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packageFullName* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

O nome completo do pacote.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Cada processo recebe o evento de [**retomada**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Pode ser útil para os desenvolvedores percorrer como seus aplicativos respondem a esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
