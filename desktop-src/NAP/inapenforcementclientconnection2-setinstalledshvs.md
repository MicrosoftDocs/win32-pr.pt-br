---
title: Método INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Usado pelo agente NAP para definir os SHVs (validadores da integridade do sistema) instalados no cliente.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Método SetInstalledShvs NAP
- Método SetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086500"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>Método INapEnforcementClientConnection2:: SetInstalledShvs

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **SetInstalledShvs** é usado pelo agente NAP para definir os SHVs (validadores da integridade do sistema) instalados no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de no\]
</dt> <dd>

Um valor de [SystemHealthEntityCount](nap-datatypes.md) que especifica o número de SHVs a serem instalados em *IDs*.

</dd> <dt>

*IDs* \[ do no\]
</dt> <dd>

Um ponteiro para um valor de [SystemHealthEntityId](nap-datatypes.md) que contém uma lista de IDs de SHV a serem instaladas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                  | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | O método foi bem-sucedido.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro de *contagem* era 0 (zero).<br/> |



 

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

 

 





