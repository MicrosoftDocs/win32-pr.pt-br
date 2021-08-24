---
title: ActivationFailureLoggingLevel
description: Define o detalhes das entradas do log de eventos sobre solicitações com falha para ativação e ativação do componente.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valor do Registro ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51d0f92dbf1b54d572de44e750fba20ca39954ced57b6276ecdc4b8c4e07960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855096"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Define o detalhes das entradas do log de eventos sobre solicitações com falha para ativação e ativação do componente.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD.**



| Valor | Descrição                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Use o log discricionário. Falhas de log por padrão, mas os clientes podem substituir esse comportamento especificando CLSCTX \_ NO FAILURE LOG em \_ \_ [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Este é o valor padrão. |
| 1     | Sempre registre todas as falhas, independentemente do que o cliente especificou.                                                                                                                                                      |
| 2     | Nunca registre falhas, independentemente do que o cliente especificou.                                                                                                                                                       |



 

Se você precisar de um aplicativo para controlar o log de eventos, é recomendável definir esse valor como 0 e escrever o código do cliente para substituí-lo quando necessário. É altamente recomendável não definir o valor como 2. Se o log de eventos estiver desabilitado, será mais difícil diagnosticar problemas. Para falhas de permissão de restrições de computador, em que COM não tem os bits CLSCTX, o COM tratará um valor de 0 como 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




