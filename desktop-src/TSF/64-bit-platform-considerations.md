---
title: Considerações de 64 bits
description: Com o aumento da disponibilidade do Windows de 64 bits, os usuários esperam métodos de entrada, como teclados internacionais em várias linguagens ou IMEs (Input Method Editors) em idiomas do leste asiático, para funcionar corretamente com os aplicativos de 32 bits e de 64 bits.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- TSF (estrutura de serviços de texto), Windows de 64 bits
- TSF (estrutura de serviços de texto), Windows de 64 bits
- serviços de texto, Windows de 64 bits
- Windows de 64 bits
- TSF (estrutura de serviços de texto), IME (editor de método de entrada)
- TSF (estrutura de serviços de texto), editor de método de entrada (IME)
- serviços de texto, editor de método de entrada (IME)
- Input Method Editor (IME)
- IME (editor de método de entrada)
- TSF (estrutura de serviços de texto), teclados internacionais
- TSF (estrutura de serviços de texto), teclados internacionais
- serviços de texto, teclados internacionais
- teclados internacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366179"
---
# <a name="64-bit-considerations"></a>Considerações de 64 bits

Com o aumento da disponibilidade do Windows de 64 bits, os usuários esperam métodos de entrada, como teclados internacionais em várias linguagens ou IMEs (Input Method Editors) em idiomas do leste asiático, para funcionar corretamente com os aplicativos de 32 bits e de 64 bits. Ao desenvolver componentes de método de entrada ou serviços de texto para o Microsoft Windows, é importante considerar o Windows de 64 bits como uma plataforma de destino potencial para seu produto.

Como os IMEs e os serviços de texto (baseados na estrutura de serviços de texto) normalmente são implementados como DLLs (bibliotecas de vínculo dinâmico), é importante observar que as DLLs são criadas especificamente para uso em ambientes de 32 bits ou em ambientes de 64 bits; uma DLL criada para uso em ambientes de 32 bits não pode ser usada por aplicativos de 64 bits e vice-versa.

> [!Note]  
> O WOW64 não atenua essa restrição de DLL específica de bit. Para obter informações sobre o WOW64, consulte [executando aplicativos de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).

 

Este tópico discute considerações de design importantes para o desenvolvimento de IMEs e serviços de texto para uso em janelas de 64 bits.

## <a name="64-bit-considerations-for-imes"></a>Considerações de 64 bits para IMEs

Esta seção descreve as considerações especiais envolvidas na criação de IMEs para uso com o Windows de 64 bits. Para obter informações sobre IMEs, consulte [Editor de método de entrada](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Compilando versões de 32 bits e de 64 bits de um IME

Devido ao problema de compatibilidade de 32 bits/64 bits mencionado anteriormente com DLLs, algumas precauções devem ser tomadas para garantir que os IMEs trabalhem de forma transparente com qualquer aplicativo (32 bits ou 64 bits) em execução em janelas de 64 bits. A solução recomendada para habilitar o IME para trabalhar de forma transparente com os aplicativos de 32 bits e 64 bits em uma plataforma de 64 bits é criar e instalar versões paralelas de 32 bits e de 64 bits da DLL do IME. Normalmente, os desenvolvedores criam DLLs paralelas de uma única fonte ajustando as configurações da plataforma de destino em seu ambiente de compilação. Para obter mais informações sobre aplicativos de 32 bits e 64 bits de fornecimento único, confira [preparando-se para o Windows de 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Instalação lado a lado de editores de método de entrada de 64 bits e 32 bits

Os desenvolvedores de IMEs e serviços de texto devem estar cientes das considerações de 64 bits descritas em todo este tópico. Felizmente, os usuários finais desses serviços não precisam se preocupar com esses detalhes específicos da implementação. Um recurso do Windows de 64 bits é a capacidade de ocultar a necessidade de versões específicas de 64 bits e 32 bits das DLLs do IME dos usuários finais. Quando ambas as versões do IME são instaladas corretamente de maneira lado a lado, o Windows de 64 bits reconhece a presença de versões de 64 bits e de 32 bits do IME e apresenta esses IMEs específicos de bits ao usuário final como um único IME *lógico* . Quando um usuário final precisa usar um IME, o Windows de 64 bits escolhe de forma transparente a versão do IME (32 bits ou 64 bits) que é apropriada para as circunstâncias determinadas.

Para instalações lado a lado de IMEs de 64 bits e 32 bits para funcionar corretamente (ou seja, para representar as duas DLLs específicas de plataforma como um único IME lógico para o usuário), as seguintes condições devem ser atendidas:

-   Os desenvolvedores devem criar versões específicas da plataforma (uma para Windows de 32 bits e outra para o Windows de 64 bits) da DLL do IME.
-   As DLLs de 32 bits e 64 bits devem compartilhar o mesmo nome de arquivo.
-   Os requisitos do diretório de instalação devem ser seguidos. Para obter mais informações, consulte Installation Directory requirements.

As instalações lado a lado das DLLs do IME de 32 bits e de 64 bits compartilham a mesma chave do registro para armazenar dados de configuração (incluindo o nome do arquivo DLL):


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



A função [**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) é usada para criar essa chave do registro. O programa de instalação e instalação para um IME deve chamar essa função para registrar o IME como um layout de teclado com suporte. A função **ImmInstallIME** deve ser chamada apenas uma vez, a partir da versão de 32 bits ou 64 bits da dll do IME.

## <a name="mismatched-ime-dlls"></a>DLLs incompatíveis do IME

A instalação somente da versão de 32 bits de um IME no Windows de 64 bits não é recomendada nem tem suporte. Se um aplicativo de 64 bits tentar carregar um IME de 32 bits, o IME falhará silenciosamente quando o aplicativo tentar carregar o layout do teclado associado.

> [!IMPORTANT]
>
> Nenhuma caixa de diálogo ou mensagem de aviso é exibida quando ocorre um erro de conflito de IME de 32 bits/aplicativo de 64 bits.

 

Considerações de 64 bits para serviços de texto

Esta seção descreve as considerações especiais envolvidas na criação de serviços de texto para uso em ambientes de 64 bits. Para obter mais informações sobre os serviços de texto e a estrutura de serviços de texto, consulte [estrutura de serviços de texto](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Criando serviços de texto de 32 bits e de 64 bits

Um serviço de texto é implementado como um objeto de Component Object Model (COM) exposto em uma DLL. Consequentemente, os conflitos de DLL de 32 bits/64 bits podem ocorrer com os serviços de texto instalados no Windows de 64 bits. Assim como acontece com os IMEs, a solução recomendada para permitir que seu serviço de texto funcione de forma transparente com os aplicativos de 32 bits e 64 bits em uma plataforma de 64 bits é criar e instalar versões paralelas de 32 bits e de 64 bits da DLL de serviço de texto.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Instalação lado a lado de serviços de texto de 64 bits e 32 bits

Para uma versão de 32 bits e uma versão de 64 bits de um serviço de texto a ser instalado lado a lado e representado ao usuário como um único serviço de texto lógico, as seguintes condições devem ser atendidas:

-   As duas versões do serviço de texto especificam o mesmo identificador de classe (CLSID) quando são registradas com o subsistema COM.
-   As duas versões do serviço de texto são registradas de forma independente. Para obter mais informações, consulte [registrando aplicativos com](/windows/desktop/com/registering-com-applications).

Quando um serviço de texto de 32 bits é registrado com o Windows de 64 bits, a operação de registro é redirecionada de forma transparente para a seguinte chave do registro:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Redirecionador de registro](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[Registro do serviço de texto](text-service-registration.md) ITfInputProcessorProfiles

A versão de 64 bits e a versão de 32 bits de um serviço de texto podem estar em uso simultaneamente. Nos casos em que ambas as versões de um serviço de texto precisam manipular objetos compartilhados, a coordenação de objetos compartilhados de acesso deve ser projetada no serviço de texto. Cada serviço de texto é responsável pelo gerenciamento de objetos compartilhados que são usados ou necessários.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Instalando somente os serviços de texto de 32 bits no Windows de 64 bits

A instalação somente da versão de 32 bits de um serviço de texto em uma plataforma de 64 bits do Windows não é recomendada nem tem suporte. Devido ao mapeamento de registro que é feito em plataformas Windows de 64 bits, um aplicativo de 64 bits pode enumerar os serviços de um serviço de texto de 32 bits por meio da interface **ITfInputProcessorProfiles** . No entanto, se um aplicativo de 64 bits tentar carregar um serviço de texto de 32 bits, a carga falhará silenciosamente.

> [!IMPORTANT]
>
> Nenhuma caixa de diálogo ou mensagem de aviso é exibida quando ocorre um erro de conflito de serviço de texto de 32 bits/aplicativo de 64 bits.

 

Outras considerações

## <a name="installation-directory-requirements"></a>Requisitos do diretório de instalação

Esta seção descreve os requisitos para onde instalar o IME e os arquivos binários do serviço de texto. Se esses requisitos não forem seguidos, seu serviço de texto ou IME talvez não funcione corretamente.

**DLLs do IME**

Em plataformas Windows de 64 bits, instale as DLLs do IME de 32 bits e 64 bits nos seguintes diretórios:

-   Instalar DLLs do IME de 32 bits no diretório do sistema do SysWOW64; Chame [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com **CSIDL \_ SYSTEMX86** para recuperar esse caminho de diretório. Como alternativa, se você estiver usando [Windows Installer](/windows/desktop/Msi/about-windows-installer), use a propriedade [**SystemFolder**](/windows/desktop/Msi/systemfolder) .
-   Instalar DLLs do IME de 64 bits no diretório do sistema system32; Chame [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)ou **SHGetFolderPath** com o [ \_ sistema CSIDL](/windows/desktop/shell/csidl) para recuperar esse caminho de diretório. Ou, por Windows Installer, use a propriedade [**System64Folder**](/windows/desktop/Msi/system64folder) .

**DLLs de serviço de texto e arquivos binários relacionados**

Em plataformas Windows de 64 bits, instale as DLLs de serviço de texto de 32 bits e 64 bits, bem como quaisquer outros arquivos binários relacionados ao seu serviço de texto ou IME nos seguintes diretórios:

-   Instalar DLLs de serviço de texto de 32 bits e quaisquer outros arquivos binários de 32 bits em um subdiretório no diretório arquivos de programas (x86); Chame **SHGetFolderPath** com **FILESX86 de \_ programa \_ CSIDL** para recuperar esse caminho de diretório. Ou, por Windows Installer, use a propriedade [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) .
-   Instale DLLs de serviço de texto de 64 bits e quaisquer outros arquivos binários de 64 bits em um subdiretório no diretório arquivos de programas; Chame **SHGetFolderPath** com **arquivos de \_ programa \_ CSIDL** para recuperar esse caminho de diretório. Ou, por Windows Installer, use a propriedade [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) .

Se você não estiver usando um pacote de Windows Installer para instalar o IME ou o serviço de texto, é altamente recommnded que você use um aplicativo de instalação de 64 bits. O redirecionador do sistema de arquivos do WOW64 pode fazer com que instaladores de 32 bits coloquem arquivos nos diretórios errados (por exemplo, o redirecionamento do sistema de arquivos do WOW64 pode fazer com que os arquivos destinados ao diretório system32 sejam instalados no diretório SysWOW64). Se você precisar usar um instalador de 32 bits, desabilite o redirecionamento de arquivo do WOW64 durante o processo de instalação para garantir que o serviço de redirecionamento de arquivo não cause nenhum redirecionamento indesejado durante o processo de instalação. Para obter informações sobre o redirecionador do sistema de arquivos do WOW64, consulte [redirecionador do sistema de arquivos](/windows/desktop/WinProg64/file-system-redirector). Para obter informações sobre como desabilitar ou habilitar o redirecionamento do sistema de arquivos do WOW64, consulte [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Evite caminhos de instalação embutidos em código. Para obter mais informações, consulte [Localizar diretórios usando a interface de programação de aplicativos que não Hard-Coded caminhos](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> Não instale nenhum arquivo de serviço de texto ou IME no diretório especial% WINDIR% \\ IME (por padrão, c: \\ Windows \\ IME). Esse diretório contém arquivos do sistema que dão suporte a serviços de texto e IMEs; Ele não deve conter nenhum arquivo de serviço de texto ou IME de terceiros, e não há suporte para o redirecionamento do sistema de arquivos do WOW64 para esse diretório.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Processos de Ctfmon.exe duplo executados em plataformas Windows de 64 bits

O processo de ctfmon.exe gerencia a estrutura de serviços de texto na área de trabalho e também fornece a interface do usuário da barra de idiomas. No Windows de 64 bits, uma versão de 32 bits e uma versão de 64 bits do processo de ctfmon.exe são executadas simultaneamente. O processo de ctfmon.exe de 64 bits gerencia serviços de texto de 64 bits e, da mesma forma, o processo de ctfmon.exe de 32 bits gerencia serviços de texto de 32 bits.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Exibir o comportamento de diferentes versões da interface do usuário da barra de idiomas

No Windows de 64 bits, somente a interface do usuário da barra de idiomas associada à versão de 64 bits de um serviço de texto é mostrada. Nos casos em que um aplicativo de 32 bits está usando a versão de 32 bits de um serviço de texto, o Windows de 64 bits insere automaticamente a interface do usuário da barra de idiomas para o serviço de texto de 64 bits equivalente. Isso garante que nenhum trabalho especial seja necessário para que os serviços de texto de 32 bits apareçam na versão de 64 bits da barra de idiomas.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Considerações sobre o painel de controle no Windows de 64 bits

o Windows de 64 bits fornece acesso a versões de 32 bits e 64 bits de serviços de texto e IMEs por meio do painel de controle. Para acessar as configurações do painel de controle para versões específicas de serviços de texto ou IMEs, examine os locais a seguir.

-   **Acesso ao painel de controle para IMEs e serviços de texto de 32 bits:** Configurações de > de inicialização – painel de controle >-> exibir ícones do painel de controle x86
-   **Acesso ao painel de controle para IMEs e serviços de texto de 64 bits:** Configurações de >-> painel de controle-> opções regionais e de idioma

Pode haver circunstâncias em que algumas configurações podem estar disponíveis apenas por meio do painel de controle de 32 bits. Nesses casos, certifique-se de que os usuários do seu serviço de texto ou IME estejam cientes disso, fornecendo a documentação apropriada ou oferecendo dicas de interface do usuário em sua interface de configurações de 64 bits.

 

 