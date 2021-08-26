---
description: A interface IESP fornece os métodos que conectam o NPP à rede, capturam o tráfego de rede para um arquivo de captura, recuperam estatísticas e desconectam o NPP da rede.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interface IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e7420e21a9f2c6ac92712326fa4a51159c6303d3972756e7a47c0797f22a1d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037426"
---
# <a name="iesp-interface"></a>Interface IESP

A interface **IESP** fornece os métodos que conectam o NPP à rede, capturam o tráfego de rede para um arquivo de captura, recuperam estatísticas e desconectam o NPP da rede. Essa interface é usada principalmente quando você precisa coletar estatísticas de [*conversa*](c.md) de rede em um formato de arquivo ESP proprietário.

## <a name="members"></a>Membros

A interface **IESP** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IESP** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IESP** tem esses métodos.



| Método                                          | Descrição                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configurar**](iesp-configure.md)             | Envia informações de configuração para uma captura<br/>                                                                         |
| [**Conectar**](iesp-connect.md)                 | Conecta o NPP à rede.<br/>                                                                                        |
| [**Desconectar**](iesp-disconnect.md)           | Desconecta o NPP da rede.<br/>                                                                                   |
| [**Getcontrolstate**](iesp-getcontrolstate.md) | Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.<br/> |
| [**Pausar**](iesp-pause.md)                     | Interrompe temporariamente a captura atual.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Recupera uma lista de todos os computadores que estão usando Monitor de Rede para capturar dados em uma sub-rede.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Recupera o status do NPP.<br/>                                                                                        |
| [**Retomar**](iesp-resume.md)                   | Retoma uma captura pausada.<br/>                                                                                               |
| [**Iniciar**](iesp-start.md)                     | Inicia a captura e cria o arquivo de captura.<br/>                                                                        |
| [**Stop**](iesp-stop.md)                       | Interrompe a captura atual.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

