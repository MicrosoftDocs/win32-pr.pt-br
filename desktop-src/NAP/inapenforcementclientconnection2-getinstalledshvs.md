---
title: Método INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Usado pelo agente NAP para consultar os SHVs (validadores da integridade do sistema) instalados no cliente.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Método GetInstalledShvs NAP
- Método GetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456026"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Método INapEnforcementClientConnection2:: GetInstalledShvs

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetInstalledShvs** é usado pelo agente NAP para consultar os SHVs (validadores da integridade do sistema) instalados no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de fora\]
</dt> <dd>

Um ponteiro para um valor de [SystemHealthEntityCount](nap-datatypes.md) que especifica o número de SHVs instalados em *IDs*.

</dd> <dt>

*IDs* \[ do fora\]
</dt> <dd>

Um ponteiro para uma matriz de valores [SystemHealthEntityId](nap-datatypes.md) que contêm as IDs SHV instaladas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                   | Descrição                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação bem-sucedida.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um argumento inválido foi passado para o método.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





