---
description: Suspende os processos do pacote se eles estão em execução no momento.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: Método IPackageDebugSettings::Suspend
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822809"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Método IPackageDebugSettings::Suspend

Suspende os processos do pacote se eles estão em execução no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packageFullName* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

O nome completo do pacote.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Esse método pode retornar um desses valores.



| Código de retorno                                                                                            | Descrição                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação foi realizada com êxito.<br/>              |
| <dl> <dt>**E \_ \_ STATECHANGE ILEGAL**</dt> </dl> | O processo não está em execução no momento.<br/> |



 

## <a name="remarks"></a>Comentários

Cada processo recebe o [**evento Suspending.**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Pode ser útil para os desenvolvedores ver como seus aplicativos respondem a esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
