---
title: Análise de despejo de memória
description: Este artigo técnico fornece informações sobre como escrever e usar um minidespejo.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075516"
---
# <a name="crash-dump-analysis"></a>Análise de despejo de memória

Nem todos os bugs podem ser encontrados antes do lançamento, o que significa que nem todos os bugs que geram exceções podem ser encontrados antes do lançamento. Felizmente, a Microsoft incluiu o SDK da plataforma uma função para ajudar os desenvolvedores a coletar informações sobre exceções descobertas pelos usuários. A função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) grava as informações de despejo de memória necessárias em um arquivo sem salvar todo o espaço do processo. Esse arquivo de informações de despejo de memória é chamado de minidespejo. Este artigo técnico fornece informações sobre como escrever e usar um minidespejo.

-   [Escrevendo um minidespejo](#writing-a-minidump)
-   [Segurança de thread](#thread-safety)
-   [Escrevendo um minidespejo com código](#writing-a-minidump-with-code)
-   [Usando Dumpchk.exe](#using-dumpchkexe)
-   [Analisando um minidespejo](#analyzing-a-minidump)
    -   [Usando o servidor de símbolos público da Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Depurando um minidespejo com o WinDbg](#debugging-a-minidump-with-windbg)
    -   [Usando ferramentas de Copy-Protection com minidespejos](#using-copy-protection-tools-with-minidumps)
-   [Resumo](#summary)

## <a name="writing-a-minidump"></a>Escrevendo um minidespejo

As opções básicas para escrever um minidespejo são as seguintes:

-   Não fazer nada. Windows gera automaticamente um minidespejo sempre que um programa gera uma exceção sem tratamento. a geração automática de um minidespejo está disponível desde o Windows XP. se o usuário permitir, o minidespejo será enviado à Microsoft, e não ao desenvolvedor, por meio de Relatório de Erros do Windows (WER). os desenvolvedores podem obter acesso a esses minidespejos por meio do [programa de aplicativo de área de trabalho Windows](../appxpkg/windows-desktop-application-program.md).

    O uso do WER requer:

    -   Desenvolvedores para assinar seus aplicativos usando Authenticode
    -   Os aplicativos têm um recurso VERSIONINFO válido em todos os executáveis e DLL

    Se você implementar uma rotina personalizada para exceções sem tratamento, será altamente recomendável usar a função [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) no manipulador de exceção para também enviar um minidespejo automatizado para o wer. A função **ReportFault** lida com todos os problemas de conexão e envio do minidespejo para o wer. Não enviar minidespejos para o WER viola os requisitos de jogos para Windows.

    para obter mais informações sobre como o WER funciona, consulte [como Relatório de Erros do Windows funciona](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). para obter uma explicação dos detalhes do registro, consulte [introdução ao Relatório de Erros do Windows](https://msdn.microsoft.com/) na [zona ISV](https://msdn.microsoft.com/)do MSDN.

-   Use um produto do Microsoft Visual Studio Team System. No menu **depurar** , clique em **Salvar despejo como** para salvar uma cópia de um despejo. O uso de um despejo salvo localmente é apenas uma opção para teste interno e depuração.
-   Adicione código ao seu projeto. Adicione a função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e o código de manipulação de exceção apropriado para salvar e enviar um minidespejo diretamente para o desenvolvedor. Este artigo demonstra como implementar essa opção. no entanto, observe que o **MiniDumpWriteDump** não funciona atualmente com código gerenciado e só está disponível no Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Acesso thread-safe

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) faz parte da biblioteca dbghelp. Essa biblioteca não é thread-safe, portanto, qualquer programa que usa **MiniDumpWriteDump** deve sincronizar todos os threads antes de tentar chamar **MiniDumpWriteDump**.

## <a name="writing-a-minidump-with-code"></a>Escrevendo um minidespejo com código

A implementação real é simples. Veja a seguir um exemplo simples de como usar o [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



Este exemplo demonstra o uso básico de [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e as informações mínimas necessárias para chamá-lo. O nome do arquivo de despejo é para o desenvolvedor; no entanto, para evitar colisões de nome de arquivo, é aconselhável gerar o nome do arquivo a partir do nome do aplicativo e do número de versão, das IDs do processo e do thread, e da data e hora. Isso também ajudará a manter os minidespejos agrupados por aplicativo e versão. Cabe ao desenvolvedor decidir quantas informações são usadas para diferenciar nomes de arquivos de minidespejo.

Deve-se observar que o nome do caminho no exemplo anterior foi gerado chamando a função [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) para recuperar o caminho do diretório designado para arquivos temporários. O uso desse diretório funciona mesmo com contas de usuário com privilégios mínimos e também impede que o minidespejo libere espaço no disco rígido depois que ele não for mais necessário.

Se você arquivar o produto durante seu processo de compilação diário, também não se esqueça de incluir símbolos para a compilação para que você possa depurar uma versão antiga do produto, se necessário. Você também precisa tomar medidas para manter as otimizações completas do compilador ao gerar símbolos. Isso pode ser feito abrindo as propriedades do projeto no ambiente de desenvolvimento e, para a configuração de versão, fazendo o seguinte:

1.  No lado esquerdo da página de propriedades do projeto, clique em C/C++. Por padrão, isso exibe as configurações **gerais** . No lado direito da página de propriedades do projeto, defina o **formato de informações de depuração** como **banco de dados do programa (/Zi)**.
2.  No lado esquerdo da página de propriedades, expanda **vinculador** e clique em **depuração**. No lado direito da página de propriedades, defina **gerar informações de depuração** como **Sim (/debug)**.
3.  Clique em **otimização** e defina **referências** para e **Liminate dados não referenciados (/OPT: REF)**.
4.  Defina **habilitar dobramento COMDAT** para **remover COMDATs redundantes (/OPT: ICF)**.

O MSDN tem informações mais detalhadas sobre a estrutura de [**\_ \_ informações de exceção de minidespejo**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) e a função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .

## <a name="using-dumpchkexe"></a>Usando Dumpchk.exe

Dumpchk.exe é um utilitário de linha de comando que pode ser usado para verificar se um arquivo de despejo foi criado corretamente. Se Dumpchk.exe gerar um erro, o arquivo de despejo estará corrompido e não poderá ser analisado. Para obter informações sobre como usar Dumpchk.exe, consulte [como usar Dumpchk.exe para verificar um arquivo de despejo de memória](https://support.microsoft.com/kb/315271/).

o Dumpchk.exe está incluído no CD do Windows XP e pode ser instalado na unidade do sistema \\ arquivos \\ de programa de suporte ferramentas \\ executando Setup.exe na \\ pasta ferramentas de suporte \\ no CD do produto Windows XP. você também pode obter a versão mais recente do Dumpchk.exe baixando e instalando as ferramentas de depuração disponíveis em [Windows ferramentas de depuração](https://www.microsoft.com/whdc/devtools/debugging/) no [Windows Hardware developer Central](https://www.microsoft.com/whdc/).

## <a name="analyzing-a-minidump"></a>Analisando um minidespejo

Abrir um minidespejo para análise é tão fácil quanto criar um.

**Para analisar um minidespejo**

1.  Abra o Visual Studio.
2.  No menu **arquivo** , clique em **abrir Project**.
3.  Defina **arquivos do tipo** para **despejar arquivos**, navegue até o arquivo de despejo, selecione-o e clique em **abrir.**
4.  Execute o depurador.

O depurador criará um processo simulado. O processo simulado será interrompido na instrução que causou a falha.

### <a name="using-the-microsoft-public-symbol-server"></a>Usando o servidor de símbolos público da Microsoft

para obter a pilha para falhas em nível de driver ou de sistema, pode ser necessário configurar Visual Studio para apontar para o servidor de símbolos público da Microsoft.

**Para definir um caminho para o servidor de símbolos da Microsoft**

1.  No menu **depurar** , clique em **Opções**.
2.  Na caixa de diálogo **Opções** , abra o nó **depuração** e clique em **símbolos**.
3.  Certifique-se **de Pesquisar os locais acima somente quando os símbolos são carregados manualmente** não estiver selecionado, a menos que você queira carregar os símbolos manualmente ao depurar.
4.  Se você estiver usando símbolos em um servidor de símbolos remoto, poderá melhorar o desempenho especificando um diretório local para o qual os símbolos podem ser copiados. Para fazer isso, insira um caminho para os **símbolos de cache do servidor de símbolo para esse diretório**. Para se conectar ao servidor de símbolos público da Microsoft, você precisa habilitar essa configuração. Observe que, se você estiver depurando um programa em um computador remoto, o diretório de cache se referirá a um diretório no computador remoto.
5.  Clique em **OK**.
6.  Como você está usando o servidor de símbolos público da Microsoft, uma caixa de diálogo de contrato de licença de usuário final é exibida. Clique em **Sim** para aceitar o contrato e baixar símbolos em seu cache local.

### <a name="debugging-a-minidump-with-windbg"></a>Depurando um minidespejo com o WinDbg

você também pode usar o WinDbg, um depurador que faz parte das ferramentas de depuração de Windows, para depurar um minidespejo. O WinDbg permite que você depure sem precisar usar Visual Studio. para baixar Windows ferramentas de depuração, consulte [Windows ferramentas de depuração](https://www.microsoft.com/whdc/devtools/debugging/) no [Windows Hardware developer Central](https://www.microsoft.com/whdc/).

depois de instalar Windows ferramentas de depuração, você deve inserir o caminho do símbolo no WinDbg.

**Para inserir um caminho de símbolo no WinDbg**

1.  No menu **arquivo** , clique em **caminho do símbolo**.
2.  Na janela **caminho de pesquisa de símbolos** , insira o seguinte:

    "SRV \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Usando ferramentas de Copy-Protection com minidespejos

Os desenvolvedores também precisam estar cientes de como seu esquema de proteção contra cópia pode afetar o minidump. A maioria dos esquemas de proteção contra cópia tem suas próprias ferramentas descramáveis e é responsabilidade do desenvolvedor saber como usar essas ferramentas com [**MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="summary"></a>Resumo

A [**função MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) pode ser uma ferramenta extremamente útil para coletar e resolver bugs após o lançamento do produto. Escrever um manipulador de exceção personalizado que usa **MiniDumpWriteDump** permite que o desenvolvedor personalize a coleção de informações e aprimora o processo de depuração. A função é flexível o suficiente para ser usada em qualquer projeto baseado em C++e deve ser considerada parte do processo de estabilidade de qualquer projeto.

 

 