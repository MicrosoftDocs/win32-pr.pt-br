---
description: Suspende os processos do pacote se eles estiverem em execução no momento.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Método IPackageDebugSettings:: Suspend'
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
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647148"
---
# <a name="ipackagedebugsettingssuspend-method"></a>Método IPackageDebugSettings:: Suspend

Suspende os processos do pacote se eles estiverem em execução no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Suspend(
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

Esse método pode retornar um desses valores.



| Código de retorno                                                                                            | Descrição                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação foi realizada com êxito.<br/>              |
| <dl> <dt>**E \_ \_ STATECHANGE ilegais**</dt> </dl> | O processo não está em execução no momento.<br/> |



 

## <a name="remarks"></a>Comentários

Cada processo recebe o evento de [**suspensão**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Pode ser útil para os desenvolvedores percorrer como seus aplicativos respondem a esse evento.

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

 

 
