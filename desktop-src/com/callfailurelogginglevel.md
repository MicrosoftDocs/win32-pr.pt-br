---
title: CallFailureLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM valor do registro CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793816"
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

 

 




