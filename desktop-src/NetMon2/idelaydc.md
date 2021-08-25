---
description: A interface IDelaydC fornece os métodos usados para se conectar à rede, capturar o tráfego de rede para um arquivo de captura, recuperar estatísticas e desconectar-se da rede.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interface IDelaydC (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1b6b965990435dd7b9a1758cc9bf8ac8001c747ae800225a90123da862032ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890556"
---
# <a name="idelaydc-interface"></a>Interface IDelaydC

A interface **IDelaydC** fornece os métodos usados para se conectar à rede, capturar o tráfego de rede para um arquivo de captura, recuperar estatísticas e desconectar-se da rede.

Essa interface captura quadros do fluxo de dados de rede e copia os quadros para um arquivo de captura. Essa interface é usada por aplicativos Monitor de Rede e NPP. Para receber os dados de rede, a NIC direcionada deve dar suporte ao modo promiscuo.

## <a name="members"></a>Membros

A interface **IDelaydC** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDelaydC** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDelaydC** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](idelaydc-configure.md)                                 | Envia informações de configuração usadas para uma captura.<br/>                                                                                        |
| [**Conectar**](idelaydc-connect.md)                                     | Conecta o NPP à rede.<br/>                                                                                                             |
| [**Desconectar**](idelaydc-disconnect.md)                               | Desconecta o NPP da rede.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Recupera informações [*de sessão*](s.md) [*e estação*](s.md) para a captura atual.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Extrai tempo, buffer, driver e outras estatísticas de rede da captura em execução no momento.<br/>                                              |
| [**Pausar**](idelaydc-pause.md)                                         | Interrompe temporariamente a captura atual.<br/>                                                                                                       |
| [**Estações de Consulta**](idelaydc-querystations.md)                         | Recupera uma lista de todos os computadores que usam Monitor de Rede para capturar dados em uma sub-rede.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Recupera o status do NPP.<br/>                                                                                                             |
| [**Retomar**](idelaydc-resume.md)                                       | Retoma uma captura em pausa.<br/>                                                                                                                    |
| [**Iniciar**](idelaydc-start.md)                                         | Inicia uma captura e cria o [*arquivo de captura*](c.md).<br/>                                                           |
| [**Stop**](idelaydc-stop.md)                                           | Interrompe a captura atual e fecha o [*arquivo de captura*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

