---
title: Método INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient.h)
description: Usado pelo Agente NAP para consultar os SHVs (Validadores de Saúde do Sistema) instalados no cliente.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- NAP do método GetInstalledShvs
- Método GetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP , método GetInstalledShvs
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
ms.openlocfilehash: 40cb18f749adc9a1b7003a777cc821fb5e003b83322a7d54c2efda4b8e5739f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939637"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Método INapEnforcementClientConnection2::GetInstalledShvs

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetInstalledShvs** é usado pelo Agente NAP para consultar os SHVs (Validadores de Saúde do Sistema) instalados no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Um ponteiro para um [valor SystemHealthEntityCount](nap-datatypes.md) que especifica o número de SHVs *instalados em ids*.

</dd> <dt>

*IDs* \[ out\]
</dt> <dd>

Um ponteiro para uma matriz de [valores SystemHealthEntityId](nap-datatypes.md) que contêm as IDs de SHV instaladas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                   | Descrição                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito na operação.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um argumento inválido foi passado para o método .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





