---
description: No exemplo a seguir, uma empresa de desenvolvimento de software hipotética chamada Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Exemplo de associação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad24c3e65ca5b297412c4a69702987cd86b5187dab63dd81435d50e7d06721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009526"
---
# <a name="file-association-example"></a>Exemplo de associação de arquivo

No exemplo a seguir, uma empresa de desenvolvimento de software hipotética chamada Litware, Inc. cria um novo player de áudio chamado LitwarePlayer. O Litware quer criar uma associação de arquivo entre LitwarePlayer e seu tipo de arquivo primário, que usa um formato de áudio desenvolvido recentemente que permite que um CD de áudio inteiro seja armazenado em menos de 10 kilobytes de memória sem perda de qualidade.

> [!IMPORTANT]
> Este tópico não se aplica a Windows 10. A maneira como as associações de arquivo padrão funcionam em Windows 10. para obter mais informações, consulte a seção sobre **alterações em como Windows 10 trata os aplicativos padrão** nesta [postagem](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Criando uma nova associação de arquivo

A empresa deve executar as etapas a seguir.

1.  **Decida se o novo tipo de arquivo deve ser tratado como público ou privado.** Esse novo tipo de arquivo é um tipo de mídia. Como os usuários trocam arquivos de mídia em várias plataformas e pode haver outros aplicativos que precisam ler o formato LitwarePlayer, um tipo de arquivo [público](fa-file-types.md) é o mais apropriado.
2.  **Determine se esse tipo de arquivo já está definido.** Verifique o banco de dados MIME da IANA (Internet Assigned Numbers Authority) e outros tipos de dados públicos de tipo de arquivo na Internet para determinar que nenhum tipo de arquivo comparável foi definido. Como esse é um novo formato de arquivo, você precisa definir um novo tipo de arquivo.
3.  **Defina uma extensão de nome de arquivo para o novo tipo de arquivo.** Os desenvolvedores escolhem o `.opa-ltw-audio` , que incorpora a abreviação de seu fornecedor e uma dica sobre o que o arquivo contém. A pesquisa determina que a extensão não está sendo usada por mais ninguém. Seguindo as recomendações atuais, nenhuma extensão curta é definida.
4.  **Defina um tipo MIME para o tipo de arquivo e registre-o com o IANA.** A Litware define o novo tipo MIME como *Audio/LitwarePlayer. 1* e prepara um aplicativo de tipo MIME, seguindo as diretrizes dispostas nos números RFC (Request for Comments) 2045, 2046, 2047 e 2048. Em seguida, eles enviam o aplicativo para o IANA, que adiciona o novo tipo de arquivo ao banco de dados de tipos MIME registrados.
5.  **Determine se existe um ProgID para o tipo de arquivo.** Como esse é um novo tipo de arquivo, não existe nenhum [ProgID](fa-progids.md) para ele. Litware sets sobre a criação de um novo ProgID para LitwarePlayer. Eles decidem o nome amigável "Player de áudio LitwarePlayer" (que é armazenado como um recurso no arquivo LitwarePlayer.exe) e criam um ícone padrão a ser usado para os arquivos associados ao LitwarePlayer (também armazenados em LitwarePlayer.exe). Como LitwarePlayer é um novo aplicativo, este é um ProgID da versão 1.
6.  **Registre o ProgID.** Quando o LitwarePlayer é instalado, o programa de instalação cria a seguinte entrada de [ProgID](fa-progids.md) no registro.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    Na chave de comando, %1 é passado como o caminho para o arquivo a ser reproduzido.

7.  **Registre a extensão de nome de arquivo para o tipo de arquivo.** Quando o LitwarePlayer é instalado, o programa de instalação cria as seguintes entradas no registro para sua extensão de tipo de arquivo personalizado.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Sempre que uma associação de arquivo é criada ou alterada, notifique o sistema de que uma alteração foi feita chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o \_ evento SHCNE assocchanged. Se isso não for feito, o Shell poderá não reconhecer nenhuma alteração feita até que o sistema seja reiniciado.

 

## <a name="additional-resources"></a>Recursos adicionais

-   [Introdução às associações de arquivo](fa-intro.md)
-   [como registrar um navegador da Internet ou cliente de Email com o Menu iniciar Windows](start-menu-reg.md)
-   [Registrando um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para associações de arquivo](fa-best-practices.md)
</dt> <dt>

[diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> <dt>

[Definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
