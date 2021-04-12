---
title: Segurança de ativação
description: Segurança de ativação
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454387"
---
# <a name="activation-security"></a>Segurança de ativação

A segurança de ativação (também chamada de segurança de inicialização) ajuda a controlar quem pode iniciar um servidor. A segurança de ativação é aplicada automaticamente pelo SCM (Gerenciador de controle de serviço) de um computador específico. Após o recebimento de uma solicitação de um cliente para ativar um objeto (conforme descrito em [funções auxiliares de criação de instância](instance-creation-helper-functions.md)), o SCM verifica a solicitação em relação às informações de segurança de ativação armazenadas em seu registro. (A segurança de ativação também é verificada para ativações de mesmo computador.)

Ao determinar a identidade do cliente, a ativação examina o sinalizador de encobrimento definido na chamada do cliente para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Se o sinalizador de encobrimento for definido (para o encobrimento dinâmico ou estático), o token de thread será usado, se presente, para determinar a identidade do cliente. Se nenhum encobrimento estiver definido, o token de processo será usado em vez do token de thread.

Para obter mais informações sobre segurança de ativação, consulte [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) e [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 