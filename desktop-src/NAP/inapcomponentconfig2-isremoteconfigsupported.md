---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para indicar se há suporte para a configuração remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Método IsRemoteConfigSupported NAP
- Método IsRemoteConfigSupported NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método IsRemoteConfigSupported
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
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918244"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>Método INapComponentConfig2:: IsRemoteConfigSupported

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **IsRemoteConfigSupported** é implementado por SHVs (validadores da integridade do sistema) para indicar se há suporte para a configuração remota.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsSupported* \[ fora\]
</dt> <dd>

Um ponteiro para um BOOL que será definido como **true** se o componente oferecer suporte à configuração remota e **false** se não tiver.

</dd> <dt>

*remoteConfigType* \[ fora\]
</dt> <dd>

Indica o tipo de configuração remota com suporte usando o valor da enumeração [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :



| Valor                                                                                                 | Significado                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) é implementado.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) é implementado. [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) e [**INapComponentConfig:: setconfig**](inapcomponentconfig-setconfig.md) podem ser chamados remotamente usando DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.

## <a name="remarks"></a>Comentários

Se nem [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nem [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) forem implementados, a configuração remota do SHV não será possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





