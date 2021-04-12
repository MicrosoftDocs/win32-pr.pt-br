---
title: InvalidSecurityDescriptorLoggingLevel
description: Define o detalhamento das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e de inicialização do componente.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- COM valor do registro InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291759"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Define o detalhamento das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e de inicialização do componente.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor | Descrição                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Sempre Registre falhas quando o COM encontrar um descritor de segurança inválido. Esse é o valor padrão.                                                                                  |
| 2     | Nunca Registre falhas quando o COM encontrar um descritor de segurança inválido. Não é recomendável desabilitar o log de eventos, pois isso pode dificultar o diagnóstico de problemas. |



 

Se você definir os descritores de segurança de permissão de acesso e inicialização (comumente chamados de ACLs) diretamente, será possível construir um descritor de segurança cujo significado não possa ser interpretado sem ambigüidade. COM faz uma entrada no log de eventos quando ele encontra um descritor de segurança inválido.

Observe que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) não têm controle sobre o log de erros de descritor de segurança inválido. Use **InvalidSecurityDescriptorLoggingLevel** para ter controle total sobre essa funcionalidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




