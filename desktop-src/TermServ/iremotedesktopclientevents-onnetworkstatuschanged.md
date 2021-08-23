---
title: Método IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Chamado quando o status da rede é alterado. | Método IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnNetworkStatusChanged
- Método OnNetworkStatusChanged Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515106"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>Método IRemoteDesktopClientEvents:: OnNetworkStatusChanged

Chamado quando o status da rede é alterado.

## <a name="syntax"></a>Sintaxe


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qualityLevel* \[ no\]
</dt> <dd>

O novo nível de qualidade da conexão. O nível de qualidade é determinado da largura de banda e dos valores de RTT (tempo de ida e volta).

Um dos valores a seguir.



| Valor                                                                        | Significado                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Não foi possível determinar o nível de qualidade.<br/>       |
| <dl> <dt>1</dt> </dl> | A qualidade da conexão é ruim (uma barra).<br/>        |
| <dl> <dt>2</dt> </dl> | A qualidade da conexão é justa (duas barras).<br/>       |
| <dl> <dt>3</dt> </dl> | A qualidade da conexão é boa (três barras).<br/>     |
| <dl> <dt>4</dt> </dl> | A qualidade da conexão é excelente (quatro barras).<br/> |



 

</dd> <dt>

*largura de banda* \[ no\]
</dt> <dd>

Especifica a nova largura de banda de conexão, em kilobits por segundo (Kbps).

</dd> <dt>

*RTT* \[ no\]
</dt> <dd>

Especifica o novo tempo de ida e volta da conexão (latência), em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





