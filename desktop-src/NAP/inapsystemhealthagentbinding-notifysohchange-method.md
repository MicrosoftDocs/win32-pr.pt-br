---
title: Método INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: É usado por SHAs quando seu SoH é alterado.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499764"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>Método INapSystemHealthAgentBinding:: NotifySoHChange

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentBinding:: NotifySoHChange** é usado por SHAs quando seu soh é alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operação bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O SHA não foi inicializado anteriormente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>     | O NapAgent foi interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.<br/> |



 

## <a name="remarks"></a>Comentários

Os SHAs não devem chamar essa API especulativamente, pois resulta em uma troca de SoH na conexão. As chamadas para essa API só devem ser feitas quando necessário.

O NapAgent não mantém esse thread para processar a alteração SoH. Em vez disso, ele retorna imediatamente e processa a alteração de forma assíncrona.

O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





