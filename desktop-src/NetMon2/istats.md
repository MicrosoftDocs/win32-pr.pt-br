---
description: A interface IStats fornece os métodos que você usa para conectar um NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede. Essa interface gera estatísticas sem quadros.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interface IStats (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27a43f8ea2902af7e2847e032da18543ffdbb228c2aa3e49fde63ce7cd727512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495006"
---
# <a name="istats-interface"></a>Interface IStats

A interface **IStats** fornece os métodos que você usa para conectar um NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede. Essa interface gera estatísticas sem quadros.

## <a name="members"></a>Membros

A interface **IStats** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IStats** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IStats** tem esses métodos.



| Método                                                                | Descrição                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](istats-configure.md)                                 | Configura o gatilho, a combinação de padrões e o tamanho do buffer do arquivo de captura.<br/>                                                                    |
| [**Conectar**](istats-connect.md)                                     | Conecta o NPP à rede.<br/>                                                                                                               |
| [**Desconectar**](istats-disconnect.md)                               | Desconecta o NPP da rede.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Recupera informações [*de sessão*](s.md) [*e estação*](s.md) sobre a captura atual.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Extrai tempo, buffer, driver e outras estatísticas de rede da captura em execução no momento.<br/>                                                |
| [**Pausar**](istats-pause.md)                                         | Interrompe temporariamente a captura atual.<br/>                                                                                                         |
| [**Estações de Consulta**](istats-querystations.md)                         | Recupera uma lista de todos os computadores que estão usando Monitor de Rede para capturar dados em uma sub-rede.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Recupera o status do NPP.<br/>                                                                                                               |
| [**Retomar**](istats-resume.md)                                       | Reinicia uma captura em pausa.<br/>                                                                                                                     |
| [**Iniciar**](istats-start.md)                                         | Inicia a captura.<br/>                                                                                                                            |
| [**Stop**](istats-stop.md)                                           | Interrompe a captura atual.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

