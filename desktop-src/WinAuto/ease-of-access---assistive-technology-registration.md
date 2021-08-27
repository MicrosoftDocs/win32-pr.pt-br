---
title: Facilidade de Acesso de tecnologia adaptativa
description: Este artigo explica como registrar um aplicativo de acessibilidade com o Central de Facilidade de Acesso. Ele também explica como personalizar seu aplicativo de acessibilidade para que ele funcione bem com a área de trabalho segura.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 28b76356f22c8cde66bce077feea52cd267a5e71
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623282"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Facilidade de Acesso de tecnologia adaptativa

Este artigo explica como registrar um aplicativo de acessibilidade com o Central de Facilidade de Acesso. Ele também explica como personalizar seu aplicativo de acessibilidade para que ele funcione bem com a área de trabalho segura.

O Central de Facilidade de Acesso é um Painel de Controle para Microsoft Windows reúne funcionalidades para acessibilidade e facilidade de uso. Usando o Central de Facilidade de Acesso, os usuários podem configurar seus computadores para atender às suas necessidades físicas e cognitivas.

Uma função do Central de Facilidade de Acesso é ajudar os usuários a iniciar aplicativos de acessibilidade, incluindo Narrador, Teclado na Tela e Lupa. Aplicativos de terceiros registrados também aparecem no Central de Facilidade de Acesso e podem ser lançados diretamente a partir daí.

Os aplicativos de acessibilidade precisam funcionar sem problemas com a área de trabalho segura. A área de trabalho segura é a interface do usuário que aparece quando o computador está bloqueado (no logoff ou quando o usuário tiver bloqueado a área de trabalho) e quando o usuário for solicitado a permitir uma ação potencialmente não segura. Por motivos de segurança, Windows limita o software de terceiros em execução na área de trabalho segura. Se você quiser que seu aplicativo de acessibilidade seja executado na área de trabalho segura, será necessário registrar o aplicativo com o Central de Facilidade de Acesso.

## <a name="registering-with-the-ease-of-access-center"></a>Registrando com o Central de Facilidade de Acesso

Os aplicativos de acessibilidade se registram no Central de Facilidade de Acesso criando uma ou mais chaves do Registro quando o aplicativo é instalado. A tabela a seguir lista as informações contidas nas chaves do Registro.



| Nome                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obrigatório/Opcional | Linguagem      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Nome do Aplicativo            | O nome do aplicativo, que está em um arquivo de recurso. Esse valor do Registro contém uma cadeia de caracteres em um formato especificado. Essa pode ser uma versão localizada do nome do aplicativo, se o aplicativo estiver localizado em idiomas diferentes do inglês. O nome aparece na Central de Facilidade de Acesso.<br/>                                                                                                                                                                                                                                                                                       | Obrigatório          | Localizada     |
| ATExe                       | O nome do arquivo executável do aplicativo ou da imagem. Windows usa esse valor para determinar se o aplicativo de acessibilidade está em execução.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obrigatório          | Não localizado |
| CopySettingsToLockedDesktop | Um **valor DWORD** que indica se é preciso copiar as configurações do aplicativo de acessibilidade para a área de trabalho bloqueada.<br/> Se esse valor for 1, o aplicativo poderá gravar configurações em um local no registro de usuário e Windows copia as configurações para o mesmo local no registro de usuário para a área de trabalho bloqueada. Isso permite que o aplicativo persista seu estado da área de trabalho "normal" para a área de trabalho bloqueada.<br/>                                                                                                                                                             | Opcional           | Não localizado |
| Descrição                 | Uma breve descrição do aplicativo, de um arquivo de recurso. Esse valor do Registro contém uma cadeia de caracteres em um formato especificado. Essa pode ser uma versão localizada da descrição, se o aplicativo estiver localizado em idiomas diferentes do inglês. O comprimento dessa cadeia de caracteres deve ser menor que 512 caracteres.<br/> A descrição aparece no Central de Facilidade de Acesso para fornecer informações adicionais sobre o aplicativo de acessibilidade para o usuário.<br/> Esse valor também pode ser usado para notificar o usuário de que o aplicativo não é usado na área de trabalho segura.<br/>      | Obrigatório          | Localizada     |
| Perfil                     | Um pequeno trecho de XML que especifica as acomodações que o aplicativo fornece. Ele garante que o aplicativo apareça na categoria correta no Central de Facilidade de Acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Obrigatório          | Não localizado |
| PassiveAutoStartBehavior    | <p>Um **valor DWORD** que indica se o comportamento de início automático herdado está habilitado.</p><p>O valor padrão é 0, o que indica que um AT requer um comportamento de início automático herdado. Isso faz com que a configuração "Iniciar após a entrada" desse AT seja verificada no OOBE (Experiência Inicial Inicial) e no Painel de Controle (consulte **Painel de Controle -> Facilidade de Acesso -> Central de Facilidade de Acesso -> Alterar** configurações de entrada) e inicia automaticamente o AT após o UAC e a tela de bloqueio.</p><p>Um valor de 1 indica que o AT deve usar o novo comportamento de início automático em que a configuração "Iniciar após a entrada" para essa AT não está marcada na OOBE (Experiência Inicial Inicial) e Painel de Controle e o AT é iniciado automaticamente uma vez por sessão do usuário (no logon) somente se a configuração "iniciar após a entrada" estiver marcada.</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Opcional          | Não localizado |
| SecureDesktopAccommodation  | O nome de um aplicativo de acessibilidade alternativo a ser executado na área de trabalho segura no lugar deste aplicativo. A alternativa pode ser um aplicativo diferente, uma versão diferente do mesmo aplicativo, um dos aplicativos de acessibilidade incluídos no Windows ou "nenhum" se você não quiser executar nenhum aplicativo de acessibilidade na área de trabalho segura. <br/>                                                                                                                                                                                                               | Opcional           | Não localizado |
| Perfil Simples              | Um valor que descreve como classificar o aplicativo em uma ou duas palavras: Leitor de tela, Lupa ou Teclado na tela, por exemplo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Obrigatório          | Não localizado |
| StartExe                    | O caminho completo do executável. Esse valor é usado para iniciar o aplicativo de acessibilidade.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obrigatório          | Não localizado |
| StartParams                 | Argumentos de linha de comando. Esses valores são usados junto com StartExe para iniciar o aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Opcional           | Não localizado |
| TerminateOnDesktopSwitch    | Um **valor DWORD** que especifica como o aplicativo de acessibilidade responde às transições de ou para a área de trabalho segura.<br/> Se esse valor não existir ou for 1, Windows encerrará e reiniciará o aplicativo em cada transição para ou da área de trabalho segura. Esse é o comportamento padrão.<br/> Se esse valor for 0, Windows encerrará o aplicativo de acessibilidade em uma transição de área de trabalho. O aplicativo continua sendo executado na área de trabalho anterior e Windows uma nova instância na nova área de trabalho se uma instância ainda não estiver em execução lá.<br/> | Opcional           | Não localizado |


 

### <a name="localization"></a>Localização

Os valores do Registro de Nome do Aplicativo e Descrição precisam ser localizáveis para dar suporte Interface de Usuário Multilíngue (MUI).

Essas cadeias de caracteres estão no formato a seguir, em que colchetes angulares significam elementos necessários e colchetes significam um elemento opcional.

*@<ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*

*<ResDllPath \\ ResDLLFilename>* é o caminho para a DLL do recurso. O caminho pode conter variáveis ambientais.

*<resID>* é a ID do recurso para a cadeia de caracteres.

*\[ O \] comentário* contém comentários opcionais.

Veja um exemplo:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Para obter mais informações sobre a MUI, [consulte Windows Centro de Conhecimento da MUI.](../intl/about-multilingual-user-interface.md)

### <a name="hci-profile"></a>Perfil HCI

O perfil HCI (Interação Com o Computador Humano) é uma maneira de determinar quais acomodações fornecer com base nas necessidades do usuário. Os aplicativos de acessibilidade devem registrar informações sobre o tipo de deficiência que o aplicativo ajuda a acomodar.

O valor do registro de perfil contém XML que descreve o tipo de deficiência de destino do aplicativo de acessibilidade. Esse XML tem o seguinte formato:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Os valores válidos para o atributo **tipo de acomodação** são os seguintes:

-   visão leve
-   visão severa
-   percepção leve
-   cognitiva severo
-   destreza leve
-   destreza severa
-   audição leve
-   audição severa
-   Fala leve
-   Fala severa

> [!Note]  
> Estes valores diferenciam maiúsculas de minúsculas.

 

Se um aplicativo de acessibilidade oferecer suporte a várias acomodações, o valor do registro de perfil deverá incluir um atributo de **tipo de acomodação** para cada acomodação.

### <a name="ease-of-access-registry-details"></a>Detalhes do registro de facilidade de acesso

Para registrar seu aplicativo de acessibilidade, você precisa criar uma chave para seu aplicativo no local do registro a seguir e preenchê-lo com pares de nome-valor.

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATs\\**

Nomeie a chave do registro do seu aplicativo usando o seguinte formato:

*"CompanyName \_ NomeDoProduto \_ v \# "*

Por exemplo, "Contoso \_ lupa \_ v 2.0".

Para adicionar valores de registro, o programa de instalação deve estar em execução com privilégios elevados.

### <a name="secure-desktop-accommodation"></a>Acomodação de área de trabalho segura

A chave do registro **SecureDesktopAccommodation** permite especificar como seu aplicativo de acessibilidade responde à área de trabalho segura. Por padrão, a central de facilidade de acesso iniciará seu aplicativo na área de trabalho segura se ele já estiver em execução na área de trabalho normal ou se estiver configurado para ser executado na área de trabalho de logon. Usando a chave **SecureDesktopAccommodation** , você pode:

-   Especifique uma versão alternativa do seu aplicativo para uso na área de trabalho segura. Por exemplo, você pode ter uma versão alternativa que desabilita recursos não seguros ou é otimizado para usar menos memória e ser iniciado mais rapidamente.

    Para especificar a versão alternativa, defina a chave **SecureDesktopAccommodation** como o nome da versão alternativa. Por exemplo, se você registrou seu aplicativo na chave do leitor de tela da Contoso \_ \_ v 1.0, você poderia registrar a versão alternativa na tela da Contoso \_ ReaderSecure \_ v 1.0. Em seguida, defina a chave **SecureDesktopAccommodation** do Contoso \_ Screen Reader \_ v 1.0 como "Contoso \_ Screen ReaderSecure \_ v 1.0".

-   Especifique um aplicativo de acessibilidade da Microsoft para usar na área de trabalho segura em vez de seu aplicativo. Para essa opção, defina **SecureDesktopAccommodation** como o nome do aplicativo de acessibilidade da Microsoft específico: "OSK", "magnifierpane" ou "Narrator".
-   Especifique que o aplicativo não deve ser executado na área de trabalho segura e nenhum aplicativo alternativo. Para essa opção, defina **SecureDesktopAccommodation** como "None" (recomendado) ou o nome de um aplicativo inexistente.

se a chave do registro **SecureDesktopAccommodation** para seu aplicativo de acessibilidade especificar um aplicativo de acessibilidade da Microsoft para ser executado na área de trabalho segura em vez de seu aplicativo, o Windows notificará o usuário sobre isso ao fazer a transição para a área de trabalho segura. para notificar o usuário, Windows exibe a cadeia de caracteres especificada na chave do registro de descrição para seu aplicativo. Por exemplo, se o aplicativo ScreenReader Deluxe 1,0 usar o Microsoft Narrator na área de trabalho segura, ele incluiria uma cadeia de caracteres de descrição como "o Microsoft Narrator será usado nos desktops bloqueados, de logon e em outras áreas de trabalho seguras no lugar do ScreenReader Deluxe 1,0".

Se a chave **SecureDesktopAccommodation** do seu aplicativo for definida como "None", use a tecla **Description** para informar ao usuário que seu aplicativo não está disponível na área de trabalho segura e nenhuma alternativa é fornecida.

Windows exibe o texto de descrição nos locais relevantes na central de facilidade de acesso.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Em execução na instalação e na área de trabalho de logon

se você acrescentar o nome de chave registrado do aplicativo de acessibilidade à cadeia de caracteres no seguinte local do registro, Windows iniciará o aplicativo imediatamente após a instalação. além disso, Windows executará automaticamente o aplicativo sempre que a área de trabalho de logon estiver ativa.

**\\configuração de \\ acessibilidade do HKCU Software Microsoft \\ Windows NT \\ CurrentVersion \\ \\**

A chave de configuração é uma cadeia de caracteres delimitada por vírgula. para adicionar seu aplicativo, acrescente uma cadeia de caracteres que seja igual à chave do registro do seu aplicativo em HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATs \\ .

### <a name="running-in-a-job"></a>Executando em um trabalho

se a chave do registro **TerminateOnDesktopSwitch** não estiver presente ou estiver definida como diferente de zero, Windows executará o aplicativo no contexto de um trabalho, encerrando e reiniciando o aplicativo com cada transição da área de trabalho. A execução em um trabalho garante que apenas uma única instância do aplicativo seja executada em um determinado momento e libera o aplicativo de ter que monitorar o estado da área de trabalho. As desvantagens da execução em um trabalho incluem:

-   O aplicativo incorre em um custo de inicialização com cada transição da área de trabalho.
-   O aplicativo só pode ser iniciado por meio da central de facilidade de acesso.
-   O aplicativo deve salvar suas configurações continuamente, pois ele pode ser encerrado a qualquer momento por uma transição de área de trabalho.

se a chave **TerminateOnDesktopSwitch** existir e for definida como 0, Windows não executará o aplicativo de acessibilidade em um trabalho. Tem estas vantagens:

-   Nenhum custo de inicialização é associado a transições de área de trabalho.
-   O aplicativo pode ser iniciado fora do centro de facilidade de acesso.

As desvantagens de não estar em execução em um trabalho incluem:

-   Como o aplicativo não é reiniciado em transições de área de trabalho, ele deve detectar quando a área de trabalho atual está inativa e responder adequadamente. Por exemplo, o aplicativo deve ceder o controle do hardware para que a versão da área de trabalho segura do aplicativo possa usá-lo, e o aplicativo deve entrar no modo de suspensão para evitar o uso de recursos do processador.
-   se o aplicativo puder ser iniciado por meio do menu Iniciar, do Windows Explorer ou da linha de comando, o centro de facilidade de acesso precisará ser informado. para obter mais informações, consulte a **tecla de logotipo Windows + U**.
-   Como várias cópias do aplicativo podem ser executadas simultaneamente em áreas de trabalho diferentes, o aplicativo deve ser escrito para dar suporte a várias cópias em execução.

### <a name="windows-logo-key--u"></a>Windows Tecla de logotipo + U

Se seu aplicativo de acessibilidade estiver configurado para ser executado em um trabalho, o código de inicialização do aplicativo deverá incluir uma chamada para a função [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) para determinar se o aplicativo está iniciando em um trabalho. Se for, o aplicativo deverá iniciar o centro de facilidade de acesso e, em seguida, sair. O exemplo a seguir mostra como chamar **IsProcessInJob**.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Se o aplicativo de acessibilidade estiver configurado para ser executado fora de um trabalho, ele deverá notificar o centro de facilidade de acesso que o aplicativo está iniciando e continuar normalmente.

Independentemente de como o aplicativo é configurado, se ele fornece uma maneira de sair de dentro do aplicativo, como um botão fechar, o aplicativo deve notificar o centro de facilidade de acesso que ele está saindo.

um aplicativo notifica a central de facilidade de acesso definindo uma chave de registro temporária e, em seguida, injetando a tecla de logotipo Windows + a combinação de tecla U no fluxo de entrada.

O aplicativo deve criar a chave temporária no seguinte local.

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**

A chave temporária deve ter o mesmo nome que o nome do aplicativo registrado, como "o \_ leitor de tela da Contoso \_ v 1.0". O valor da chave é um **DWORD** definido como 0x0003 quando está sendo iniciado, ou 0x0002 quando o aplicativo está sendo encerrado.


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Windows Tecla de logotipo + volume acima

quando o usuário inicia seu aplicativo de acessibilidade pressionando a tecla de logotipo Windows + combinação de teclas de configuração (como em um dispositivo de tablet), a facilidade de acesso passa o seguinte argumento de linha de comando para o aplicativo:

**/hardwarebuttonlaunch**

Seu aplicativo pode usar esse argumento para determinar se deve iniciar normalmente ou ajustar o comportamento de acordo.

### <a name="transferring-secure-desktop-settings"></a>Transferindo configurações de área de trabalho segura

Se seu aplicativo de acessibilidade der suporte à área de trabalho segura, você poderá usar o registro para copiar as configurações quando o aplicativo passar para a área de trabalho segura. A cópia das configurações ajuda a tornar a transição para a área de trabalho segura mais direta para o usuário.

Para copiar as configurações, defina a chave do registro CopySettingsToLockedDesktop do aplicativo como 1 e armazene as configurações no seguinte local do registro.

**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**

A central de facilidade de acesso monitora esse local do registro enquanto o aplicativo está em execução. Quando ocorre uma transição para a área de trabalho segura, a central de facilidade de acesso copia as configurações para o mesmo local no hive HKCU da área de trabalho segura. O aplicativo pode, então, ler as configurações e retomar seu estado.

Seu aplicativo de acessibilidade deve gravar suas configurações em intervalos regulares ou sempre que os valores forem alterados. A gravação de configurações na saída do aplicativo não funcionará. Se o aplicativo estiver sendo executado em um trabalho, ele será encerrado na transição para fora da área de trabalho segura, antes que o código de saída tenha a oportunidade de ser executado. Se o aplicativo não estiver em execução em um trabalho, o aplicativo não será encerrado na transição para fora da área de trabalho segura.

### <a name="caution"></a>Cuidado

Como as chaves do Registro descritas aqui são gravadas no modo de usuário, elas não são seguras. Se o seu aplicativo de acessibilidade ler o conteúdo dessas chaves, ele deverá verificar cuidadosamente os dados e usá-los com cautela. Especificamente, o aplicativo deve fazer uma verificação de limites em valores **DWORD** , ter cuidado com comprimentos de cadeia de caracteres, não deve ler nomes de DLL de plug-in e não deve executar nenhum comando encontrado em cadeias.

## <a name="registry-examples"></a>Exemplos de registro

O exemplo a seguir mostra os valores de registro possíveis para um produto fictício chamado contoso ScreenReader versão 2,0, cujo nome localizado é armazenado como um recurso.

Os valores na tabela estão sob a seguinte chave:

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ acessibilidade \\ ATs \\ Contoso \_ Screen Reader \_ v 2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Type</th>
<th>Dados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Descrição</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Narrator</td>
</tr>
</tbody>
</table>



 

Se o aplicativo fornecer um leitor de tela e uma lupa de tela em um único executável, os valores para o componente de leitor de tela poderão ter esta aparência:



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Type</th>
<th>Dados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-30</td>
</tr>
<tr class="even">
<td>Descrição</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Arquivos de Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Os valores para o componente lupa seriam na seguinte chave:

**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATs \\ Contoso \_ lupa \_ v 2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Type</th>
<th>Dados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-31</td>
</tr>
<tr class="even">
<td>Descrição</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Amplia</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Arquivos de Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

