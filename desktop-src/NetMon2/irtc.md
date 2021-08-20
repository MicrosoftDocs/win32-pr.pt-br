---
description: A interface IRTC fornece os métodos usados para conectar o NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interface IRTC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132925"
---
# <a name="irtc-interface"></a>Interface IRTC

A interface **IRTC** fornece os métodos usados para conectar o NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede. **IRTC** Obtém uma interface para pontos de entrada somente locais, que são necessários para envolver a captura em tempo real. Essa interface inclui um método que transmite um retorno de chamada para o NPP.

## <a name="members"></a>Membros

A interface **IRTC** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRTC** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IRTC** tem esses métodos.



| Método                                                              | Descrição                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](irtc-configure.md)                                 | Define o gatilho, a correspondência de padrões e o tamanho do buffer da captura.<br/>                                                                             |
| [**Conectar**](irtc-connect.md)                                     | Conecta o NPP à rede.<br/>                                                                                                             |
| [**Desconectar**](irtc-disconnect.md)                               | Desconecta o NPP da rede.<br/>                                                                                                        |
| [**Getcontrolstate**](irtc-getcontrolstate.md)                     | Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Recupera informações de [*sessão*](s.md) e de [*estação*](s.md) para a captura atual.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Extrai tempo, buffer, Driver e outras estatísticas de rede da captura em execução no momento.<br/>                                              |
| [**Pausar**](irtc-pause.md)                                         | Interrompe temporariamente a captura atual.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Recupera uma lista de todos os computadores em uma sub-rede que estão usando Monitor de Rede para capturar dados de rede.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Recupera o status do NPP.<br/>                                                                                                             |
| [**Retomar**](irtc-resume.md)                                       | Reinicia uma captura pausada.<br/>                                                                                                                   |
| [**Iniciar**](irtc-start.md)                                         | Inicia uma captura.<br/>                                                                                                                            |
| [**Stop**](irtc-stop.md)                                           | Interrompe a captura atual.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

