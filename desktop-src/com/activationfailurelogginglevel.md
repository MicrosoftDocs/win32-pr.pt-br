---
title: ActivationFailureLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre solicitações com falha para inicialização e ativação do componente.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- COM valor do registro ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364443"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Define o detalhamento das entradas do log de eventos sobre solicitações com falha para inicialização e ativação do componente.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor | Descrição                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Use o registro em log discricionário. Falhas de log por padrão, mas os clientes podem substituir esse comportamento especificando \_ CLSCTX \_ nenhum \_ log de falha em [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Este é o valor padrão. |
| 1     | Sempre Registre todas as falhas, independentemente do que o cliente especificou.                                                                                                                                                      |
| 2     | Nunca registre nenhuma falha, independentemente do que o cliente especificou.                                                                                                                                                       |



 

Se você precisar de um aplicativo para controlar o log de eventos, é recomendável que você defina esse valor como 0 e grave o código do cliente para substituí-lo quando necessário. É altamente recomendável que você não defina o valor como 2. Se o log de eventos estiver desabilitado, será mais difícil diagnosticar problemas. Para falhas de permissão de restrições de máquina, em que COM não tem os bits CLSCTX, o COM tratará um valor de 0 como 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




