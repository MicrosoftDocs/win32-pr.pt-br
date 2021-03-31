---
title: Controle de conta de usuário e BITS
description: Quando um usuário administrador faz logon no computador, dois tokens de acesso são criados. Um é um token de acesso de usuário padrão filtrado e o outro é um token de acesso de administrador completo.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 3017b3a0d816ba393d1427c5c1d2315a68b2dcc0
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2020
ms.locfileid: "103917071"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Segurança de BITS, tokens e contas de administrador

## <a name="http-server-certificate-callbacks"></a>Retornos de chamada de certificado do servidor HTTP
A validação correta de certificados de servidor é uma parte fundamental da manutenção da segurança HTTPS. O BITS ajuda a sempre validar certificados de servidor em uma lista de requisitos especificados por [**SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). Por padrão, o BITS usa a validação de certificado de estilo "navegador".

Você também pode especificar uma função personalizada para chamar a fim de validar ainda mais o certificado. Defina o retorno de chamada do certificado do servidor com o método [**SetServerCertificateValidationInterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) . Seu método só será chamado depois que o sistema operacional tiver validado o certificado com base na chamada do [ **SetSecurityFlag** s](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) . 

## <a name="http-client-certificates"></a>Certificados de cliente HTTP
Você pode definir um certificado de cliente em um trabalho HTTP com dois métodos de configurações de certificado diferentes. Você pode definir um certificado por [ID](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) ou pelo [nome da entidade](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)do certificado. O certificado do cliente será usado durante a negociação TLS (ou renegociação) se o servidor exigir autenticação de cliente.

## <a name="write-only-http-headers"></a>Cabeçalhos HTTP somente gravação
O BITS ajuda a proteger tokens de autenticação HTTP de acesso indesejado. Geralmente, um servidor HTTP precisará de algum tipo de token de segurança ou cadeia de caracteres ao baixar ou carregar um arquivo em servidores HTTP.

O BITS protege esses tokens de autenticação de várias maneiras.
* O BITS permite que você use conexões HTTP protegidas por TLS e SSL especificando uma URL HTTPS.
* Os cabeçalhos personalizados sempre são persistidos em um formato criptografado no disco.
* Você pode impedir que cabeçalhos de clientes sejam retornados para outros programas com o método [**IBackgroundCopyJobHttpOptions3:: MakeCustomHeadersWriteOnly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) .


## <a name="standard-and-administrator-users"></a>Usuários padrão e administrador
Um usuário que está no grupo de administradores pode executar um processo com acesso de usuário padrão ou em um estado elevado (com privilégios de administrador). O BITS executará o trabalho em qualquer Estado, desde que o usuário esteja conectado ao computador. No entanto, se o usuário criou o trabalho ou assumiu a propriedade do trabalho em um estado elevado, o usuário deve estar no estado elevado para recuperar ou modificar o trabalho (caso contrário, a chamada falhará com acesso negado (0x80070005)). Para determinar o estado elevado de um trabalho, chame o método [**IBackgroundCopyJob4:: GetOwnerElevationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) .

Um usuário padrão não pode enumerar ou modificar trabalhos pertencentes a outros usuários.

## <a name="integrity-level"></a>Nível de integridade
Além do estado elevado, o nível de integridade do token pode determinar se o usuário pode modificar um trabalho. Um cliente não pode modificar trabalhos criados por um token com um nível de integridade mais alto. Em particular, muitos tokens do sistema local carregam um nível de integridade maior que o nível de integridade de uma janela com privilégios elevados e, portanto, não podem ser modificados por um administrador de uma janela de comando com privilégios elevados. Por exemplo, Windows Update e trabalhos de SMS são executados como LocalSystem, que tem um nível de integridade mais alto do que um token elevado, para que um administrador não possa modificar ou excluir esses trabalhos. Para modificar esses trabalhos, crie uma tarefa Agendador de Tarefas que seja executada como sistema local. A tarefa pode executar um aplicativo de console que usa a API BITS, ou a tarefa pode executar um script que chama BitsAdmin.exe. Para determinar o nível de integridade usado, chame o método [**IBackgroundCopyJob4:: GetOwnerIntegrityLevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) .

## <a name="service-identity"></a>Identidade do serviço
A partir do Windows 10 pode ser 2019 atualização (10,0; Build 18362), os trabalhos do BITS iniciados a partir de um serviço manterão a identidade do serviço. Isso permite que os serviços que desejam usar o BITS baixem arquivos ou carreguem arquivos de um diretório cujas permissões estejam vinculadas ao SID do serviço. Além disso, o tráfego de rede será atribuído corretamente ao serviço que solicitou o trabalho BITS em vez de ser atribuído ao BITS.

 




