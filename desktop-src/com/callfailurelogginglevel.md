---
title: CallFailureLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM valor do registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822503"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor | Descrição                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Sempre Registre falhas durante uma chamada no processo do servidor COM.                           |
| 2     | Nunca Registre falhas durante uma chamada no processo do servidor COM. Esse é o valor padrão. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




