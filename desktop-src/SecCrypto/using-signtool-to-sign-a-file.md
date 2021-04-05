---
description: Explica como usar SignTool para assinar um arquivo.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Usando SignTool para assinar um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090914"
---
# <a name="using-signtool-to-sign-a-file"></a>Usando SignTool para assinar um arquivo

O comando a seguir assina o arquivo chamado MyControl.exe usando um [*certificado*](../secgloss/c-gly.md) armazenado em um arquivo de troca de informações pessoais (pfx):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo PFX protegido por senha:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Certifique-se de proteger a senha corretamente.

 

Os seguintes sinais de comando e carimbo de data/hora do arquivo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Para obter informações sobre o carimbo de data/hora de um arquivo após ele já ter sido assinado, consulte [adicionando carimbos de data/hora aos arquivos assinados anteriormente](adding-time-stamps-to-previously-signed-files.md).

 

O comando a seguir assina o arquivo usando um certificado localizado no meu repositório com um nome de assunto do meu fornecedor da empresa:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

O comando a seguir assina um controle ActiveX e fornece informações que são exibidas pelo Internet Explorer quando o usuário é solicitado a instalar o controle:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado cujas informações de [*chave privada*](../secgloss/p-gly.md) são protegidas por um módulo de criptografia de hardware. Por exemplo, suponha que o certificado chamado "meu certificado de High-Value" tenha uma chave privada instalada em um módulo de criptografia de hardware e o certificado seja instalado corretamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado cujas informações de [*chave privada*](../secgloss/p-gly.md) são protegidas por um módulo de criptografia de hardware. Um repositório de computador é especificado para o repositório da AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo. As informações de chave privada são protegidas por um módulo de criptografia de hardware e o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e o contêiner de [*chave*](../secgloss/k-gly.md) são especificados pelo nome. Esse comando será útil se o certificado não estiver instalado corretamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) retorna um texto de linha de comando que declara o resultado da operação de assinatura. Além disso, SignTool retorna um código de saída zero para execução bem-sucedida, uma para execução com falha e duas para execução concluída com avisos.

Para obter informações sobre como verificar a assinatura de um arquivo, consulte [usando Signtool para verificar uma assinatura de arquivo](using-signtool-to-verify-a-file-signature.md). Para obter informações sobre como adicionar um carimbo de data/hora se o arquivo já tiver sido assinado, consulte [adicionando carimbos de data/hora aos arquivos assinados anteriormente](adding-time-stamps-to-previously-signed-files.md). Para obter informações adicionais sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).

 

 
