---
title: Perguntas frequentes sobre EAP
description: Encontre respostas para perguntas frequentes (FAQs) sobre as APIs de EAP, como ' Qual é o tempo de vida de uma autenticação EAP? '.
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a8b424ed195d30621c67007fc8e7d1a0882bae6ce676c70a1ca0dc93e8b846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978526"
---
# <a name="eap-frequently-asked-questions"></a>Perguntas frequentes sobre EAP

O tópico a seguir fornece respostas para perguntas frequentes sobre as APIs de EAP.



| Pergunta                                                                                        | Resposta                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Qual é o tempo de vida de uma autenticação EAP?                                                  | Em uma situação típica, a autenticação consiste em tudo o que ocorre entre chamar as funções [**RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) . Quando um usuário opta por configurar um provedor de EAP no snap-in RRAS, uma autenticação consiste em tudo o que ocorre entre chamar os métodos [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) e [**Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) .<br/> |
| O que é "política de grupo"?                                                                         | Para obter uma descrição da diretiva de grupo, consulte [política de grupo coleção](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| As funções EAP podem substituir a política de configuração especificada pela política de grupo?                      | Não, nunca. Se a política de grupo estiver em uso, as configurações da política de grupo sempre substituirão as definições de configuração de EAP.                                                                                                                                                                                                                                                                                                                                                         |
| Preciso avisar os usuários sobre tentativas de PIN inválidas. É possível capturar um código PIN inválido? | Quando o usuário insere o PIN errado, a autenticação extensível Protocol-Transport segurança de camada (EAP-TLS) enviará um código de erro para o suplicante de VPN. Depois que um código de erro é retornado, o suplicante pode implementar sua lógica de repetição preferida.                                                                                                                                                                                                                    |
| O que é o EAP-TLS (segurança de nível EAP-Transport)?                                                 | O EAP-TLS é um protocolo de cliente-servidor no qual os perfis de certificado distintos normalmente são usados para o cliente e o servidor. Para obter mais informações, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo de autenticação extensível](using-extenstible-authentication-protocol.md)
</dt> </dl>