---
title: Método getconfigid de INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de configuração em uma solicitação de validação.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Método getconfigid NAP
- Método getconfigid NAP, interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, método getconfigid
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757766"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>Método INapSystemHealthValidationRequest2:: getconfigid

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest2:: Getconfigid** é usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de configuração em uma solicitação de validação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configid* \[ fora\]
</dt> <dd>

No retorno, um ponteiro para UINT32 que contém uma ID de configuração do SHV.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com êxito.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro configid era **nulo**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





