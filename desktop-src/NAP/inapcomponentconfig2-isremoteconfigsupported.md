---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon.h)
description: É implementado por SHVs (validadores de saúde do sistema) para indicar se há suporte para a configuração remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Nap do método IsRemoteConfigSupported
- Método NAP IsRemoteConfigSupported, interface INapComponentConfig2
- INapComponentConfig2 interface NAP , método IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621763"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>Método INapComponentConfig2::IsRemoteConfigSupported

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método IsRemoteConfigSupported** é implementado por SHVs (validadores de saúde do sistema) para indicar se há suporte para a configuração remota.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isSupported* \[ out\]
</dt> <dd>

Um ponteiro para um BOOL que será definido como **TRUE se** o componente for compatível com a configuração remota e **FALSE** se não o fizer.

</dd> <dt>

*remoteConfigType* \[ out\]
</dt> <dd>

Indica o tipo de configuração remota com suporte usando o valor da [**enumeração RemoteConfigurationType:**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype)



| Valor                                                                                                 | Significado                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) é implementado.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) é implementado. [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) podem ser chamados remotamente usando DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um dos códigos de Windows padrão.

## <a name="remarks"></a>Comentários

Se [**invokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nem [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) são implementados, a configuração remota do SHV não é possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





