---
description: A lista a seguir são práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.
title: Práticas recomendadas para associações de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094211"
---
# <a name="best-practices-for-file-associations"></a>Práticas recomendadas para associações de arquivos

A lista a seguir são práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.

-   [Não copiar associações de arquivo do Registro](#do-not-copy-file-associations-from-the-registry)
-   [Evite Hard-Coding caminhos no Registro sempre que possível](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [Sempre envolver cadeias de caracteres de expansão entre aspas](#always-wrap-expanding-strings-in-quotation-marks)
-   [Não confunda a reprodução automática/a reprodução automática com associações de arquivo](#do-not-confuse-autoplayautorun-with-file-associations)
-   [Não confunda o banco de Internet Explorer MIME com associações de arquivo](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [Usar progIDs corretamente formados e com versão](#use-properly-formed-and-versioned-progids)
-   [Não usar extensões de nome de arquivo curto](#do-not-use-short-file-name-extensions)
-   [Registrar novos tipos de arquivo no banco de dados MIME do IANA](#register-new-file-types-in-the-iana-mime-database)
-   [Inscreva-se com o serviço Web Windows para associações de arquivos](#sign-up-with-the-windows-web-service-for-file-associations)
-   [Tópicos relacionados](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>Não copiar associações de arquivo do Registro

Recomendamos que você não copie associações de arquivo existentes do Registro. Isso geralmente leva à propagação de associações de arquivos mal formadas. Em vez disso, você deve seguir as etapas descritas em Cenário [de exemplo de associação de arquivo](fa-sample-scenarios.md).

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>Evite Hard-Coding caminhos no Registro sempre que possível

Assim como caminhos de codificação em programas podem causar problemas, os caminhos de codificação no Registro também podem levar a problemas. Em vez disso, você deve usar cadeias de caracteres de expansão do Registro (REG EXPAND SZ) para fornecer independência de caminho \_ \_ quando aplicável. Por exemplo, em vez de usar este método:

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

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>Sempre envolver cadeias de caracteres de expansão entre aspas

A expansão de cadeias de caracteres pode conter espaços quando elas se expandem. Como os espaços geralmente são interpretados como delimitadores de argumento, eles causam problemas em determinadas circunstâncias. Por exemplo, um comando para invocar MyProgram pode ser armazenado no Registro como:

`%SYSTEMROOT%\MyProgram %1 %2`

MyProgram espera que %1 seja o caminho completo para um nome de arquivo e %2 é uma opção para indicar alguma ação. Se esse comando for executado com os argumentos C: Arquivos de **\\ Programas Meus Documentos \\ \\document.txt** **e /print** e supondo um SYSTEMROOT de C: \\ WINNT, ele se expandirá para:

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

Nesse caso, MyProgram interpreta que o primeiro argumento é C: Programa e o segundo argumento é Arquivos Meu, que não \\ \\ é o comportamento pretendido. No entanto, os argumentos são interpretados corretamente, independentemente de conterem espaços, se as cadeias de caracteres em expansão são envolvidas entre aspas da seguinte maneira:

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>Não confunda a reprodução automática/a reprodução automática com associações de arquivo

As Associações de Arquivos são semelhantes à Reprodução Automática/Autorun de algumas maneiras. No entanto, o Autoplay/Autorun oferece recursos separados e distintos daqueles fornecidos por associações de arquivos. Para obter mais [informações, consulte Criando um aplicativo CD-ROM habilitado para AutoRun.](autoplay.md)

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>Não confunda o banco de Internet Explorer MIME com associações de arquivo

As Associações de Arquivos são semelhantes Windows Internet Explorer banco de dados MIME, no qual os tipos de arquivo podem (e devem) incluir uma definição de tipo MIME. No entanto, o Internet Explorer de dados MIME é separado e distinto das associações de arquivo.

## <a name="use-properly-formed-and-versioned-progids"></a>Usar progIDs corretamente formados e com versão

Sempre use [ProgIDs com versão](fa-progids.md), mesmo que haja apenas uma versão do ProgID. ProgIDs com controle de versão ajudam a evitar conflitos e substituições de ProgID. Eles também permitem que diferentes versões de um aplicativo co existam.

## <a name="do-not-use-short-file-name-extensions"></a>Não usar extensões de nome de arquivo curto

Extensões de nome de arquivo longo oferecem as seguintes vantagens:

-   O comprimento limitado de extensões curtas as torna propensas a *colisões de extensão.* Uma colisão de extensão ocorre quando a mesma extensão é usada para classificar vários tipos de arquivo. O uso de extensões longas reduz significativamente as chances de uma colisão.
-   Nomes de arquivo curtos tendem a ser um pouco criptográficos. Extensões longas tendem a ser mais significativas porque informações adicionais podem ser inseridas na extensão.

Para obter mais informações, consulte [extensões de nome de arquivo](fa-file-extensions.md).

## <a name="register-new-file-types-in-the-iana-mime-database"></a>Registrar novos tipos de arquivo no banco de dados MIME do IANA

A IANA (Internet Assigned Numbers Authority) mantém um banco de dados público de tipos MIME registrados. Ao definir um novo tipo de arquivo público, recomendamos que você também defina um tipo MIME para o tipo de arquivo e registre esse tipo com o IANA. Não há nenhum custo para o registro.

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>Inscreva-se com o serviço Web Windows para associações de arquivos

Os desenvolvedores de aplicativos podem se inscrever com o Windows Web que os usuários usam para encontrar aplicativos que podem operar em tipos de arquivo específicos. O processo para inscrever-se no serviço Web é detalhado Windows sistema de associação de arquivos [no processo de entrada](https://support.microsoft.com/kb/929149).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[Diretrizes para gerenciar aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> <dt>

[Definir acesso ao programa e padrões de computador (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 



