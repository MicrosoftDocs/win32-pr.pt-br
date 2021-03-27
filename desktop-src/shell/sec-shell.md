---
description: Este tópico fornece informações sobre considerações de segurança relacionadas ao shell do Windows.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Considerações de segurança: Shell do Microsoft Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647536"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Considerações de segurança: Shell do Microsoft Windows

Este tópico fornece informações sobre considerações de segurança relacionadas ao shell do Windows. Este documento não pode fornecer tudo o que você precisa saber sobre problemas de segurança — em vez disso, use-o como ponto de partida e referência para essa área de tecnologia específica.

O Shell controla diversos aspectos importantes do sistema, incluindo vários que apresentam possíveis riscos de segurança se eles não forem tratados adequadamente. Este tópico descreve alguns dos problemas mais comuns e como solucioná-los em seus aplicativos. Lembre-se de que a segurança não está limitada a explorações baseadas na Internet. Em sistemas compartilhados, incluindo sistemas acessíveis por meio dos serviços de terminal, você também deve garantir que os usuários não possam fazer nada que possa danificar outras pessoas que compartilham o sistema.

-   [Instalando o aplicativo corretamente](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [Preenchimento automático](#autocomplete)
-   [ShellExecute, ShellExecuteEx e funções relacionadas](#shellexecute-shellexecuteex-and-related-functions)
-   [Movendo e copiando arquivos](#moving-and-copying-files)
-   [Gravando extensões de namespace seguro](#writing-secure-namespace-extensions)
-   [Alertas de segurança](#security-alerts)
-   [Tópicos relacionados](#related-topics)

## <a name="installing-your-application-properly"></a>Instalando o aplicativo corretamente

A maioria dos possíveis problemas de segurança do shell pode ser atenuada com a instalação correta do aplicativo.

-   Instale o aplicativo na pasta arquivos de programas. 

    | Sistema Operacional                             | Localização                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 e anterior | arquivos de \_ programa CSIDL \_                                                                                                                                                                                                                      |
    | Windows Vista e posterior                      | FOLDERid \_ ProgramFiles, FolderId \_ PROGRAMFILESX86, FolderId \_ ProgramFilesX64, FolderId \_ ProgramFilesCommon, FOLDERid \_ ProgramFilesCommonX86 ou FolderId \_ ProgramFilesCommonX64. Consulte [**KNOWNFOLDERID**](knownfolderid.md) para obter informações específicas. |

    

     

-   Não armazene os dados do usuário na pasta arquivos de programas.

    Use a pasta de dados apropriada para dados comuns a todos os usuários.

    

    | Sistema Operacional                             | Localização               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 e anterior | AppData comuns de CSIDl \_ \_ |
    | Windows Vista e posterior                      | PASTA de \_ ProgramData  |

    

     

    Use a pasta de dados de usuário apropriada para dados que pertencem a um usuário específico.

    

    | Sistema Operacional                             | Localização                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 e anterior | CSIDl \_ de AppData, CSIDL \_ pessoal e outros.               |
    | Windows Vista e posterior                      | FOLDERid \_ RoamingAppData, documentos FolderId \_ e outros. |

    

     

-   Se você precisar instalar o em um local diferente da pasta arquivos de programas, certifique-se de definir as listas de controle de acesso (ACLs) corretamente para que os usuários não tenham acesso a partes inadequadas do sistema de arquivos. Todos os dados específicos de um usuário específico devem ter uma ACL que impede que qualquer outro usuário o acesse.
-   Ao configurar as associações de arquivo, certifique-se de especificar corretamente a linha de comando. Use um caminho totalmente qualificado e empacote quaisquer elementos que contenham espaço em branco entre aspas. Empacote os parâmetros do comando em aspas separadas. Caso contrário, a cadeia de caracteres poderá ser analisada incorretamente e o aplicativo não será iniciado corretamente. Dois exemplos de linhas de comando formadas corretamente são mostrados aqui.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> O local das pastas de instalação padrão pode variar de sistema para sistema. Para obter o local de uma pasta padrão em um sistema específico do Windows Vista ou posterior, chame [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) com o valor [**KNOWNFOLDERID**](knownfolderid.md) apropriado. No Windows XP, no Windows Server 2003 ou em sistemas anteriores, chame [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com o valor [**CSIDL**](csidl.md) apropriado.

 

## <a name="shlwapi"></a>Shlwapi

A API leve do Shell (shlwapi) inclui várias funções de manipulação de cadeia de caracteres. Usar essas funções incorretamente pode levar a cadeias de caracteres truncadas inesperadamente sem nenhuma notificação do truncamento que está sendo retornado. Nos casos a seguir, as funções shlwapi não devem ser usadas. As funções alternativas listadas, que apresentam menos riscos, devem ser usadas em seu lugar.



| Função shlwapi                                                 | Função alternativa                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw),[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) e funções relacionadas             |
| [**Strcpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw), [ **strcpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) e funções relacionadas         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) e funções relacionadas |



 

Com funções como [**PathRelativePathTo**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) que retornam um caminho de arquivo, sempre defina o tamanho do buffer para o máximo de \_ caracteres de caminho. Isso garante que o buffer seja grande o suficiente para manter o maior caminho de arquivo possível, além de um caractere nulo de terminação.

Para obter mais informações sobre as funções de cadeia de caracteres alternativas, consulte [about strsafe. h](../menurc/strsafe-ovw.md).

## <a name="autocomplete"></a>Preenchimento automático

Não use o recurso de preenchimento automático para senhas.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx e funções relacionadas

Há várias funções do shell que você pode usar para iniciar aplicativos: [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)e [**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Certifique-se de fornecer uma definição não ambígua do aplicativo a ser executado.

-   Ao fornecer o caminho do arquivo executável, forneça o caminho totalmente qualificado. Não dependem do Shell para localizar o arquivo.
-   Se você fornecer uma cadeia de caracteres de linha de comando que contenha espaço em branco, coloque a cadeia de caracteres entre aspas. Caso contrário, o analisador pode interpretar um único elemento que contém espaços como vários elementos.

## <a name="moving-and-copying-files"></a>Movendo e copiando arquivos

Uma chave para a segurança do sistema é atribuir ACLs corretamente. Você também pode usar arquivos criptografados. Certifique-se de que, ao mover ou copiar arquivos, eles recebam a ACL correta e que eles não tenham sido descriptografados acidentalmente. Isso inclui a movimentação de arquivos para a **Lixeira**, bem como dentro do sistema de arquivos. Use [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista ou posterior) ou [**SHFILEOPERATION**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP e versões anteriores). Não use [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile), que pode não definir a ACL esperada para o arquivo de destino.

## <a name="writing-secure-namespace-extensions"></a>Gravando extensões de namespace seguro

As extensões de namespace do shell são uma maneira poderosa e flexível de apresentar dados ao usuário. No entanto, eles podem causar falha do sistema se não forem gravados corretamente. Alguns pontos importantes a serem considerados:

-   Não presuma que dados como imagens estão formatados corretamente.
-   Não presuma que \_ o caminho máximo é equivalente ao número de *bytes* em uma cadeia de caracteres. É o número de *caracteres*.

## <a name="security-alerts"></a>Alertas de segurança

A tabela a seguir lista alguns recursos que podem, se usados incorretamente, comprometer a segurança de seus aplicativos.



| Recurso                                                                        | Atenuação                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Pesquisas que dependem da verificação de uma série de locais padrão para localizar um arquivo específico podem ser usadas em um ataque de falsificação. Use um caminho totalmente qualificado para garantir que você acesse o arquivo desejado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | O primeiro argumento, *psz1*, deve ser grande o suficiente para manter *psz2* e o fechamento ' \\ 0 '; caso contrário, pode ocorrer uma saturação de buffer. Em vez disso, use uma das alternativas a seguir. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**StrCatBuff**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | Não há garantia de que a cadeia de caracteres final seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**StrCatChainW**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | Não há garantia de que a cadeia de caracteres final seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | O primeiro argumento, *psz1*, deve ser grande o suficiente para manter *psz2* e o fechamento ' \\ 0 '; caso contrário, pode ocorrer uma saturação de buffer. Em vez disso, use uma das alternativas a seguir. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)ou [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | Não há garantia de que a cadeia de caracteres copiada seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) pressupõe que *lpsz* é uma cadeia de caracteres terminada em nulo. Além disso, não há garantia de que a cadeia de caracteres retornada seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)ou [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | O primeiro argumento, *pszFront*, deve ser grande o suficiente para manter *pszBack* e o fechamento ' \\ 0 '; caso contrário, pode ocorrer uma saturação de buffer. Lembre-se de que o último argumento, *cchMax*, é o número de caracteres a serem copiados em *pszFront*, não necessariamente o tamanho do *pszFront* em bytes. Em vez disso, use uma das alternativas a seguir. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)ou [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | Não há garantia de que a cadeia de caracteres copiada seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)ou [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | Não há garantia de que a cadeia de caracteres copiada seja terminada em nulo. Em vez disso, use uma das alternativas a seguir. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)ou [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Centro de desenvolvedores de segurança](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerators](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[TechCenter de segurança](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[Sobre o strsafe. h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
