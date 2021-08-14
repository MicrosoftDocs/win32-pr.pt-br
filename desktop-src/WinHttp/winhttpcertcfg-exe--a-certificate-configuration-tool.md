---
description: a ferramenta de configuração de certificado do Microsoft Windows HTTP Services (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, permite que os administradores instalem e configurem certificados de cliente em qualquer repositório de certificados que possa ser acessado pela conta do gerenciador de aplicativos da Web do servidor da Internet (IWAM). A ferramenta também elimina a necessidade de fazer qualquer coisa especial para contas como a conta IWAM para obter acesso aos certificados ao usar páginas de Active Server (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, uma ferramenta de configuração de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ce9978f6e2ffcafa1357a45dbeff80c12bf0e6ea2f7f3fb9656376b33dfb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743794"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, uma ferramenta de configuração de certificado

a ferramenta de configuração de certificado do [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", permite que os administradores instalem e configurem certificados de cliente em qualquer [*repositório de certificados*](glossary.md) que possa ser acessado pela conta do gerenciador de aplicativos da Web do servidor da Internet (IWAM). A ferramenta também elimina a necessidade de fazer qualquer coisa especial para contas como a conta IWAM para obter acesso aos certificados ao usar páginas de Active Server (ASP).

O MMC (console de gerenciamento Microsoft) permite que os administradores importem certificados de cliente para um computador local. No entanto, a importação de um certificado não concede automaticamente acesso à chave privada para outras contas. Essa chave privada é necessária para a autenticação de certificado do cliente. a ferramenta de configuração de certificado do Microsoft Windows HTTP Services (WinHTTP) fornece a capacidade de conceder acesso a contas adicionais, como a conta IWAM, quando necessário.

-   [Usando a ferramenta de configuração de certificado](#using-the-certificate-configuration-tool)
-   [Exemplos](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Usando a ferramenta de configuração de certificado

a ferramenta de configuração de certificado WinHTTP, WinHttpCertCfg.exe, está disponível como um download no site de [ferramentas do Kit de recursos do Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . O código de exemplo a seguir mostra os parâmetros de linha de comando válidos a serem usados com essa ferramenta.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

A tabela a seguir lista os parâmetros para a ferramenta de configuração do.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Exibe dados de sintaxe.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>especifica que o certificado deve ser importado de um arquivo de informações pessoais Exchange (PFX). Esse parâmetro deve ser seguido pelo nome do arquivo. Quando esse parâmetro é especificado, &quot; -a &quot; e &quot; -c &quot; também devem ser especificados.</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Especifica que o acesso é concedido a uma chave privada. Quando esse parâmetro é especificado, &quot; -a &quot; , &quot; -c e &quot; &quot; -s &quot; também devem ser especificados.</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Especifica que o acesso é removido para uma chave privada. Quando esse parâmetro é especificado, &quot; -a &quot; , &quot; -c e &quot; &quot; -s &quot; também devem ser especificados.</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Especifica que as contas com acesso a uma chave privada estão listadas. Quando esse parâmetro é especificado, &quot; -c &quot; e &quot; -s &quot; também devem ser especificados.</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Especifica a conta de usuário no computador que está sendo configurado. Pode ser um computador local ou uma conta de domínio, como &quot; IWAM_TESTMACHINE &quot; , &quot; testuser &quot; ou &quot; TESTDOMAIN\DOMAINUSER &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Especifica o local e o nome do <a href="glossary.md"><em>repositório de certificados</em></a>. Use &quot; local_machine &quot; ou &quot; CURRENT_USER &quot; para designar qual ramificação do Registro usar para o local. O <em>repositório de certificados</em> pode ser qualquer instalado no computador. Os exemplos de nome típicos são &quot; My &quot; , &quot; root &quot; e &quot; TrustedPeople &quot; . O local e o nome do <em>repositório de certificados</em> são separados por uma barra invertida, por exemplo, &quot; local_machine \root &quot; .
<blockquote>
[!Note]<br />
Embora a &quot; &quot; ramificação CURRENT_USER do registro possa ser especificada com esse parâmetro, estender o acesso às chaves privadas destina-se principalmente a certificados instalados em um <a href="glossary.md"><em>repositório de certificados</em></a> do computador local que pode ser acessado por vários usuários.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Especifica uma cadeia de caracteres de pesquisa que não diferencia maiúsculas de minúsculas para localizar o primeiro certificado enumerado com um nome de entidade que contém essa subcadeia de caracteres.</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Especifica uma senha que é usada para importar o certificado e a chave privada. Isso só é usado com a opção de importação.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> O usuário deve ter privilégios suficientes para usar essa ferramenta, o que exige que o usuário seja um administrador e o mesmo usuário que instalou o certificado do cliente, se estiver instalado.
>
> A ferramenta "WinHttpCertCfg.exe" não é útil para configurar certificados armazenados em um sistema de arquivos, como FAT32, que não oferece suporte a ACLs (listas de controle de acesso).

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram algumas das maneiras como a ferramenta de configuração pode ser usada.

1.  Esse comando lista as contas que têm acesso à chave privada para o certificado "myCertificate" no [*repositório de certificados*](glossary.md) "raiz" da \_ ramificação do computador local do registro.

    **Winhttpcertcfg-l-c \_ raiz do computador local \\ -s myCertificate**

2.  Esse comando concede acesso à chave privada do certificado "myCertificate" no [*repositório de certificados*](glossary.md) "My" para a conta testuser.

    **Winhttpcertcfg-g-c \_ computador local \\ My-s myCertificate-a testuser**

3.  Esse comando importa um certificado e uma chave privada de um arquivo PFX e estende o acesso à chave privada para outra conta.

    **Winhttpcertcfg-i PFXFile-c \_ máquina local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**

4.  Esse comando nega o acesso à chave privada para a conta IWAM \_ TESTMACHINE com o certificado especificado.

    **Winhttpcertcfg-r-c \_ raiz do computador local \\ -s myCertificate-a IWAM \_ TESTMACHINE**

 

 




