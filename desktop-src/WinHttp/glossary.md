---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glossário (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2064d9b7424971e2be286b18129fa3b4109fb64a03fa26ababc152a5cf0b64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133199"
---
# <a name="glossary-winhttp"></a>Glossário (WinHTTP)

<dl> <dt>

<span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**dados de autenticação**
</dt> <dd>

Bloco de dados específico do esquema que é trocado entre o servidor e o cliente durante a autenticação. Para provar sua identidade, o cliente criptografa alguns ou todos esses dados com um nome de usuário e senha. O cliente envia os dados criptografados para o servidor, o que descriptografa os dados e os compara com o original. Se os dados descriptografados corresponderem aos dados originais, o cliente será autenticado.

</dd> <dt>

<span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**codificação Base64**
</dt> <dd>

Esquema usado para transmitir dados binários. A base64 processa dados como grupos de 24 bits, mapeando esses dados para quatro caracteres codificados. Às vezes, ele é chamado de codificação de 3 a 4. Cada 6 bits do grupo de 24 bits é usado como um índice em uma tabela de mapeamento (o alfabeto Base64) para obter um caractere para os dados codificados. Os dados codificados têm comprimentos de linha limitados a 76 caracteres.

</dd> <dt>

<span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**repositório de certificados**
</dt> <dd>

Normalmente, o armazenamento permanente em que certificados, CRL (listas de certificados revogados) e listas de certificados confiáveis (CTL) são armazenados. Um repositório de certificados também pode ser temporário ao trabalhar com certificados baseados em sessão.

</dd> <dt>

<span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**co-branding**
</dt> <dd>

Capacidade de um site Microsoft Passport participante fornecer seus próprios elementos de identidade visual e explicações sobre as páginas de serviço de rede do Passport. A comarcação inclui personalizar a aparência, o texto específico e o comportamento específico nas páginas da rede do Passport.

</dd> <dt>

<span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**página de código**
</dt> <dd>

Tabela que relaciona os códigos de caracteres binários usados por um programa a chaves no teclado ou à aparência de caracteres no monitor. O uso de páginas de código é uma maneira de fornecer suporte a conjuntos de caracteres e layouts de teclado usados em diferentes países e regiões. Você pode configurar dispositivos como o monitor e o teclado para usar uma página de código específica e alternar de uma página de código (como Estados Unidos) para outra (como, por exemplo, Portugal) na solicitação do usuário.

</dd> <dt>

<span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**
</dt> <dd>

O verbo HTTP (ou o método HTTP) é uma instrução enviada em uma mensagem de solicitação que notifica um servidor HTTP sobre a ação a ser executada no recurso especificado. Por exemplo, "GET" especifica que um recurso está sendo recuperado do servidor. Os verbos comuns incluem "GET", "POST" e "HEAD". Para obter mais informações e uma lista completa de verbos HTTP padrão, consulte a especificação HTTP/1.1.

</dd> <dt>

<span id="term_ticket"></span><span id="TERM_TICKET"></span>**concessão**
</dt> <dd>

Cookie que contém um perfil de usuário para autenticação do Passport. Cada tíquete corresponde a uma URL. O servidor de logon de uma autoridade de domínio do Passport fornece tíquetes que o cliente envia a um membro do Passport para autenticação.

</dd> <dt>

<span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente do usuário**
</dt> <dd>

O agente do usuário é o aplicativo cliente que solicita um documento de um servidor HTTP. Quando o cliente envia uma solicitação para um servidor HTTP, normalmente ele envia o nome do agente do usuário com o cabeçalho da solicitação para que o servidor possa determinar os recursos do software cliente.

</dd> </dl>

 

 



