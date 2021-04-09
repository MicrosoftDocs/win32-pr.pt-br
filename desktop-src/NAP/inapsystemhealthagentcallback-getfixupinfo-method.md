---
title: Método INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para determinar o estado do agente de integridade do sistema, enquanto ele está processando um SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Método GetFixupInfo NAP
- Método GetFixupInfo NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085709"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>Método INapSystemHealthAgentCallback:: GetFixupInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback:: GetFixupInfo** é chamado pelo NapAgent para determinar o estado do agente de integridade do sistema, enquanto ele está processando um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*informações* \[ do fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que contém o status de correção do agente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

O agente de integridade do sistema deve retornar **S \_ OK** imediatamente sem bloqueio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





