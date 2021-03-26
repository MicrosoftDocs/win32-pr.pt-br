---
description: A lista a seguir é recomendada práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.
title: Práticas recomendadas para associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501570"
---
# <a name="best-practices-for-file-associations"></a>Práticas recomendadas para associações de arquivo

A lista a seguir é recomendada práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.

-   [Não copie associações de arquivo do registro](#do-not-copy-file-associations-from-the-registry)
-   [Evite caminhos de Hard-Coding no registro sempre que possível](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Sempre encapsular cadeias de caracteres em expansão entre aspas](#always-wrap-expanding-strings-in-quotation-marks)
-   [Não confunda reprodução automática/autorun com associações de arquivo](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Não confunda o banco de dados MIME do Internet Explorer com associações de arquivo](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usar ProgIDs corretamente formados e com controle de versão](#use-properly-formed-and-versioned-progids)
-   [Não usar extensões de nome de arquivo curto](#do-not-use-short-file-name-extensions)
-   [Registrar novos tipos de arquivo no banco de dados MIME do IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Inscreva-se com o serviço Web do Windows para associações de arquivos](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Tópicos relacionados](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Não copie associações de arquivo do registro

Recomendamos que você não copie as associações de arquivo existentes do registro. Isso geralmente leva à propagação de associações de arquivo formadas inadequadamente. Em vez disso, você deve seguir as etapas descritas no [cenário de exemplo Associação de arquivo](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evite caminhos de Hard-Coding no registro sempre que possível

Assim como os caminhos de código fixo em programas podem causar problemas, os caminhos de código fixo no registro também podem causar problemas. Em vez disso, você deve usar cadeias de caracteres de expansão do registro (REG \_ Expand \_ SZ) para fornecer independência de caminho quando aplicável. Por exemplo, em vez de usar este método:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

Você deve usar este método:

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Sempre encapsular cadeias de caracteres em expansão entre aspas

A expansão de cadeias de caracteres pode conter espaços quando eles são expandidos. Como os espaços são frequentemente interpretados como delimitadores de argumento, eles causam problemas em determinadas circunstâncias. Por exemplo, um comando para invocar myprogram pode ser armazenado no registro como:

`%SYSTEMROOT%\MyProgram %1 %2`

Myprogram espera que %1 seja o caminho completo para um nome de arquivo e %2 é uma opção para indicar alguma ação. Se esse comando for executado com **os argumentos C: \\ arquivos de programas \\ meus documentos \\document.txt** e **/Print** e supondo uma raiz_do_sistema de C: \\ WinNT, ele se expandirá para:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

Nesse caso, myprogram interpreta que o primeiro argumento é C: \\ Program, e o segundo argumento é files \\ My, que não é o comportamento pretendido. Os argumentos são interpretados corretamente, no entanto, independentemente de conterem espaços, se as cadeias de caracteres em expansão forem encapsuladas entre aspas da seguinte maneira:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Não confunda reprodução automática/autorun com associações de arquivo

As associações de arquivo são semelhantes à reprodução automática/autorun de algumas maneiras. No entanto, a reprodução automática/autorun oferece instalações separadas e distintas das fornecidas pelas associações de arquivo. Para obter mais informações, consulte [criando um aplicativo de CD-ROM habilitado para autorun](autoplay.md).

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Não confunda o banco de dados MIME do Internet Explorer com associações de arquivo

As associações de arquivo são semelhantes ao banco de dados MIME do Windows Internet Explorer, em que os tipos de arquivo podem (e devem) incluir uma definição de tipo MIME. No entanto, o banco de dados MIME do Internet Explorer é separado e distinto das associações de arquivo.

## <a name="use-properly-formed-and-versioned-progids"></a>Usar ProgIDs corretamente formados e com controle de versão

Sempre use [ProgIDs com versão](fa-progids.md), mesmo se houver apenas uma versão do ProgID. ProgIDs com versão ajudam a evitar conflitos e substituições de ProgID. Eles também permitem que versões diferentes de um aplicativo coexistam.

## <a name="do-not-use-short-file-name-extensions"></a>Não usar extensões de nome de arquivo curto

Extensões de nome de arquivo longo oferecem as seguintes vantagens:

-   O comprimento limitado de extensões curtas as torna propensos a *colisões de extensão.* Uma colisão de extensão ocorre quando a mesma extensão é usada para classificar vários tipos de arquivo. O uso de extensões longas diminui significativamente as chances de uma colisão.
-   Nomes de arquivo curtos tendem a ser um pouco confusos. As extensões longas tendem a ser mais significativas porque informações adicionais podem ser inseridas na extensão.

Para obter mais informações, consulte [extensões de nome de arquivo](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrar novos tipos de arquivo no banco de dados MIME do IANA

A IANA (Internet Assigned Numbers Authority) mantém um banco de dados público de tipos MIME registrados. Ao definir um novo tipo de arquivo público, recomendamos que você também defina um tipo MIME para o tipo de arquivo e registre esse tipo com o IANA. Não há nenhum custo para o registro.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Inscreva-se com o serviço Web do Windows para associações de arquivos

Os desenvolvedores de aplicativos podem se inscrever no serviço Web do Windows que os usuários usam para localizar aplicativos que podem operar em tipos de arquivo específicos. O processo de inscrição com o serviço Web é detalhado no [processo de integração do sistema de associação de arquivos do Windows](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[Diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> <dt>

[Definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



