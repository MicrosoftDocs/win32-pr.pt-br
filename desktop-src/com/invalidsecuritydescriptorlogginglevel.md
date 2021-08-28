---
title: InvalidSecurityDescriptorLoggingLevel
description: Define o detalhes das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e início de componente.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valor do Registro InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c2362b38c19acd8d895e5fa9640475fa401a7d5bd88c8016056df2d22c3a579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854336"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Define o detalhes das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e início de componente.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD.**



| Valor | Descrição                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Sempre registre falhas quando COM encontrar um descritor de segurança inválido. Esse é o valor padrão.                                                                                  |
| 2     | Nunca registre falhas quando COM encontrar um descritor de segurança inválido. Não é recomendável desabilitar o log de eventos, pois isso pode dificultar o diagnóstico de problemas. |



 

Se você definir descritores de segurança de permissão de acesso e início (normalmente chamados de ACLs) diretamente, será possível construir um descritor de segurança cujo significado não pode ser interpretado de forma não ambígua. O COM faz uma entrada de log de eventos quando encontra um descritor de segurança inválido.

Observe que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) não têm controle sobre o registro em log de erros inválidos do descritor de segurança. Use **InvalidSecurityDescriptorLoggingLevel** para ter controle total sobre essa funcionalidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




