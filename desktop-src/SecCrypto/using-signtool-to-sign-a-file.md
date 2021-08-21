---
description: Explica como usar o SignTool para assinar um arquivo.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Usando SignTool para assinar um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d8e85e8e22f65ccbe8b5f15453b0a0cac34fc27697bad648b1c815f255b10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971466"
---
# <a name="using-signtool-to-sign-a-file"></a>Usando SignTool para assinar um arquivo

O comando a seguir assina o arquivo [](../secgloss/c-gly.md) chamado MyControl.exe usando um certificado armazenado em um arquivo PFX (Personal Information Exchange) :

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo PFX protegido por senha:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Certifique-se de proteger corretamente a senha.

 

O comando a seguir assina e carimbos de data/hora do arquivo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Para obter informações sobre o carimbo de data/hora de um arquivo depois que ele já tiver sido assinado, consulte [Adicionando carimbos de data/hora a arquivos assinados anteriormente.](adding-time-stamps-to-previously-signed-files.md)

 

O comando a seguir assina o arquivo usando um certificado localizado em Minha loja com um nome de assunto de My Company Publisher:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

O comando a seguir assina um controle ActiveX e fornece informações que são exibidas pelo Internet Explorer quando o usuário é solicitado a instalar o controle:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado [*cujas informações de chave*](../secgloss/p-gly.md) privada são protegidas por um módulo de criptografia de hardware. Por exemplo, suponha que o certificado chamado "Meu certificado High-Value", tenha uma chave privada instalada em um módulo de criptografia de hardware e o certificado seja instalado corretamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado [*cujas informações de chave*](../secgloss/p-gly.md) privada são protegidas por um módulo de criptografia de hardware. Um armazenamento de computador é especificado para o armazenamento [*da*](../secgloss/c-gly.md) AC (autoridade de certificação).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo. As informações de chave privada são protegidas por um módulo de criptografia [](../secgloss/k-gly.md) de hardware e o CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) e o contêiner de chave são especificados pelo nome. Esse comando será útil se o certificado não estiver instalado corretamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) retorna o texto da linha de comando que declara o resultado da operação de assinatura. Além disso, SignTool retorna um código de saída de zero para execução bem-sucedida, um para execução com falha e dois para execução que foi concluída com avisos.

Para obter informações sobre como verificar a assinatura de um arquivo, consulte [Usando SignTool para verificar uma assinatura de arquivo](using-signtool-to-verify-a-file-signature.md). Para obter informações sobre como adicionar um carimbo de data/hora se o arquivo já tiver sido assinado, consulte [Adicionando carimbos de data/hora a arquivos assinados anteriormente.](adding-time-stamps-to-previously-signed-files.md) Para obter informações adicionais sobre [o SignTool,](signtool.md) [consulte SignTool.](signtool.md)

 

 
