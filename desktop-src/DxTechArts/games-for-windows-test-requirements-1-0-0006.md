---
title: Melhores práticas para casos de teste dos jogos para Windows no Windows XP, Windows Vista, Windows 7 e Windows 8
description: Este artigo fornece casos de teste para jogos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007872"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Jogos para casos de teste do Windows: práticas recomendadas para jogos no Windows XP, Windows Vista, Windows 7 e Windows 8

Este artigo fornece casos de teste para jogos para Windows.

## <a name="how-to-use-this-article"></a>Como usar esse artigo?

Há três seções principais para este artigo:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de teste**
</dt> <dd>

Cada requisito de teste neste documento tem quatro seções principais: um título e uma tabela com três seções notáveis (coluna esquerda, direita superior, direita inferior).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Nome do caso de teste.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Caixa, coluna da extrema esquerda
</dt> <dd>

Nomes dos sistemas operacionais aos quais se aplica o caso de teste.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, direita superior
</dt> <dd>

Breve resumo do caso de teste.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, direita inferior
</dt> <dd>

Detalhes do caso de teste real.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Exemplo de script de teste**
</dt> <dd>

Esta seção é um exemplo da sequência que uma etapa de teste típica seguiria se estiver usando os requisitos de teste como um guia.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas da ferramenta de teste**
</dt> <dd>

Esta seção contém observações detalhadas sobre cada uma das ferramentas de teste usadas para verificar condições de aprovação ou falha nos requisitos de teste.

</dd> </dl>

## <a name="test-requirements"></a>Requisitos de teste

### <a name="1-game-requirements"></a>1. requisitos do jogo

### <a name="11-windows-games-explorer"></a>1,1 explorador de jogos do Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>O jogo deve estar visível no explorador de jogos no Windows Vista e no Windows 7. Quando selecionado, o jogo também deve exibir metadados corretos. A instalação não deve criar um atalho para iniciar o jogo na área de trabalho, no menu iniciar ou em qualquer outro local. Tarefas e atalhos para remoção não devem ser criados.</td>
</tr>
<tr class="even">

<td><ol>
<li>Depois de instalar o jogo, abra o explorador de jogos.</li>
<li>Verifique se o ícone de jogo é exibido no explorador de jogos.</li>
<li>Clique com o botão direito do mouse no ícone e teste a & tarefa de suporte de reprodução definida pelo aplicativo.</li>
<li>Clique no ícone e verifique se os metadados (Publicador, desenvolvedor, gênero, data de lançamento, versão) na parte inferior são exibidos e estão corretos.</li>
<li>Verifique se o ícone de jogo exibe informações do WEI (índice de experiência do Windows) no explorador de jogos.</li>
<li>Verifique se os hiperlinks de jogos para os metadados funcionam corretamente no explorador de jogos. (Se os hiperlinks não aparecerem, esse é um sinal possível para o qual o exe não está assinado; consulte a <a href="#23-sign-files">seção 2,3</a>.)</li>
<li>Verifique se o jogo exibe classificação de controle dos pais preciso no explorador de jogos. (Se estiver sem classificação, verifique se esse é um jogo sem classificação; caso contrário, esse é um indicador de que o exe não está assinado; consulte a <a href="#23-sign-files">seção 2,3</a>.)</li>
<li>Verifique se o jogo não coloca os atalhos de inicialização na área de trabalho do usuário.</li>
<li>Clique em Iniciar-> todos os programas.</li>
<li>Verifique se o jogo não coloca os atalhos de inicialização no menu iniciar.</li>
<li>Verifique se o jogo não coloca os atalhos de desinstalação no menu iniciar fora do painel de controle.</li>
<li>Se o jogo for distribuído digitalmente, verifique se o provedor de serviços aparece no explorador de jogos do Windows.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1,2 controles de segurança/pais da família Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>O jogo deve ser executado dentro do contexto de um &quot; usuário padrão &quot; . Os controles dos pais devem ser capazes de bloquear o jogo. Verifique se o GDF tem nomes EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>Crie uma conta de usuário padrão no Windows Vista ou no Windows 7 chamada Toby. Iniciar-> painel de controle-> adicionar ou remover contas de usuário-> criar nova conta</li>
<li>Como Jane, da conta de administrador, configure os controles dos pais para o jogo. Iniciar-> painel de controle-> configurar controles dos pais para qualquer usuário-> Toby
<ol>
<li>Verifique se o jogo é iniciado no ícone do explorador de jogos.</li>
<li>Verifique se o jogo exibe a classificação de controle dos pais preciso abaixo do título do jogo no painel de controle dos controles dos pais.</li>
<li>Antes de aplicar os controles dos pais, verifique se o jogo não solicita as credenciais de administrador na inicialização.</li>
<li>Defina controles dos pais como &quot; ativado &quot; .</li>
<li>Na seção Configurações do Windows, clique em jogos.</li>
<li>Clique em OK (agora, a configuração deve ser ao seu com &quot; /todos os jogos &quot; ).</li>
<li>Verifique se o jogo é executado com essas configurações como o usuário Jane.</li>
<li>Faça logoff como Jane e faça logon como Toby.</li>
<li>Verifique se o jogo é executado com essas configurações como usuário Toby.</li>
<li>Faça logoff como Toby e faça logon como Jane.</li>
<li>Volte para a tela anterior e selecione &quot; definir classificações de &quot; jogo.</li>
<li><p>Selecione uma classificação inferior à classificação de ESRB do jogo.</p>
<blockquote>
[!Note]<br />
Se o jogo não for classificado, ignore esta etapa e vá para a próxima parte deste teste. Pode ser necessário escolher um sistema de classificação diferente para encontrar uma classificação de jogo, dependendo da localidade do idioma do SKU que está sendo testado.
</blockquote>
<p><br/></p></li>
<li>Faça logoff como Jane e faça logon como Toby.</li>
<li>Verifique se o jogo não é iniciado para o usuário Toby quando ESRB está bloqueado pelo usuário Jane.</li>
<li>Faça logoff como Toby e faça logon como Jane.</li>
<li>Se alterado anteriormente, restaure as configurações de ESRB.</li>
<li>Se não houver configurações de ESRB, selecione &quot; bloquear ou permitir jogos específicos &quot; e selecione o jogo por nome.</li>
<li>Faça logoff como Jane e faça logon como Toby.</li>
<li>Verifique se o jogo não é iniciado para o usuário Toby quando o EXE/Name é bloqueado pelo usuário Jane.</li>
<li>Faça logoff como Toby e volte como Jane.</li>
<li>Como Jane, abra controles de usuário-> restrições de aplicativo.</li>
<li>Clique em &quot; Toby só pode usar os programas permitidos &quot; e clicar em OK (ou seja, não permitir nenhum EXEs).</li>
<li>Ir para controles de usuário | Os jogos controlam e permitem o jogo específico usando a classificação ESRB.</li>
<li>Faça logoff como Jane e faça logon como Toby e tente jogar o jogo.</li>
<li>Verifique se o jogo não está bloqueado e se o Toby pode reproduzi-lo quando &quot; não permitir que nenhum EXEs &quot; esteja definido.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1,3 jogos sofisticados salvos no Windows Vista

Esse requisito foi desativado.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 Xbox 360 controlador comum para \[ requisito condicional do Windows\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Jogos que dão suporte a controladores de gamepad devem dar suporte ao controlador Xbox 360 para Windows usando a API XInput. Todas as referências a gatilhos e botões comuns do controlador devem usar os nomes do Xbox 360.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie o jogo.</li>
<li>Vá para as opções do controlador. **</li>
<li>Verifique se o jogo reconhece o controlador Xbox 360 para Windows como um dispositivo de entrada.</li>
<li>Jogue e verifique se o jogo e o sistema de menus são controláveis com o controlador Xbox 360 para Windows.</li>
<li>Verifique se o controlador Xbox 360 para Windows se comporta de acordo com os padrões aceitos. (B para voltar, A para aceitar, inicie o no menu do jogo/Pause ou aceite, etc.)</li>
<li>Verifique se o jogo refere-se aos botões do controlador e aos gatilhos usando os nomes do Xbox 360.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Se o jogo não dá suporte a um controlador de jogo e/ou só dá suporte ao teclado/mouse, ignore este caso de teste.
</blockquote>
<br/> * * As configurações do controlador podem estar localizadas fora do jogo. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1,5 várias taxas de proporção e resoluções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>O jogo deve dar suporte a pelo menos as seguintes taxas de proporção e resoluções de tela associadas: <br/>
<ul>
<li>4:3 &quot; normal &quot; (800 600 ou 1024 768)</li>
<li>16:9 &quot; widescreen &quot; (1280 720)</li>
<li>16:10 &quot; widescreen &quot; (1152 720, 1680 1050 ou 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Localize as opções de vídeo para o jogo (isso pode estar em nosso jogo).<br/>
<blockquote>
[!Note]<br />
Os testes a seguir devem ser feitos em um monitor widescreen.
</blockquote>
<br/>
<ol>
<li>Na seção resolução de vídeo, selecione 800 600 ou 1024 768.</li>
<li>Verifique se o jogo é executado a uma resolução de proporção de 4:3.</li>
<li>Na seção resolução de vídeo, selecione 1280 720.</li>
<li>Verifique se o jogo é executado a uma resolução de proporção de 16:9.</li>
<li>Na seção resolução de vídeo, selecione 1680 1050, 800 480 ou 1152 720.</li>
<li>Verifique se o jogo é executado a uma resolução de proporção de 16:10.</li>
<li>Verifique se o jogo não amplia a imagem e, por sua vez, apresenta uma área mais ampla de exibição.</li>
<li>Verifique se o jogo solicita o usuário quando uma alteração é feita na resolução.</li>
<li>Se o usuário não aceitar dentro de 15 segundos, verifique se a exibição é revertida para a configuração anterior.</li>
<li>Verifique se o jogo não adiciona barras pretas à esquerda e à direita da área de jogo. (Nesse caso, você verá a área do jogo ainda em uma proporção de 4:3 no meio da tela.)</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1,6 Windows Media Center

Esse requisito foi desativado.

### <a name="17-direct3d-conditional-requirement"></a>Requisito condicional de 1,7 Direct3D \[\]



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Se o jogo usar o Direct3D, a versão mínima com suporte deverá ser o Direct3D 9 e o Direct3D deverá ser o padrão para qualquer opção de configuração de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd> Inicie o jogo. Nas opções de vídeo, verifique se há opções de processamento, D3D e/ou OpenGL. Se houver, verifique se as opções de processamento do jogo são padrão para Direct3D. Se não for possível verificar se D3D9 é a versão do DirectX que está sendo usada, prossiga para o teste automatizado. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt> <dd> Usar ferramenta: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1,8 habilitar reconhecimento de DPI alta



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Jogos e seus instaladores devem ser executados corretamente sem problemas visuais quando o dimensionamento de DPI estiver habilitado.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Defina o sistema como DPI 150%: <br/> Windows Vista: painel de controle: personalização, ajustar tamanho da fonte (DPI), DPI personalizado. Defina como 150%.<br/> Windows 7: painel de controle: Exibir, definido como maior – 150%.<br/></li>
<li>Execute o processo de instalação e o jogo para verificar se não há problemas com telas recortadas ou caixas de diálogo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt> <dd> Verifique se o elemento <dpiAware>true</dpiAware> está contido no manifesto inserido.<br/> Usar ferramenta: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. segurança e compatibilidade

### <a name="21-follow-user-account-control-guidelines"></a>2,1 seguir as diretrizes de controle de conta de usuário



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Todos os arquivos executáveis (. EXE) incluído com um aplicativo deve ter um manifesto inserido que define seu nível de execução:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Para instaladores de jogos e jogos, o uiAccess sempre deve ser definido como &quot; false &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Verifique se os arquivos executáveis do jogo contêm manifestos.</li>
<li>Verifique se o manifesto do arquivo executável do jogo requestedExecutionLevel é &quot; asInvoker &quot; .</li>
</ol>
Usar ferramenta: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2,2 suporte a versões x64 do Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Para manter a compatibilidade com as versões x64 do Windows: <br/>
<ul>
<li>Os títulos e os instaladores de título não devem conter nenhum código de 16 bits nem contar com nenhum componente de 16 bits.</li>
<li>Se o jogo for dependente dos drivers do modo kernel para a operação, as versões x64 desses drivers deverão estar disponíveis. A instalação do jogo deve detectar e instalar os drivers e componentes adequados para as edições de 64 bits do Windows.</li>
</ul>
<blockquote>
[!Note]<br />
O suporte para a edição de 64 bits do Windows XP Professional é opcional.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Teste manual<br/>
<ol>
<li>Execute o jogo em edições de 64 bits do Windows. Verifique se o processo de instalação do jogo é executado normalmente em edições de 64 bits do Windows Vista ou do Windows 7.</li>
<li>Verifique se o jogo não encontrou um erro como resultado de executáveis de 16 bits em edições de 64 bits do Windows Vista ou do Windows 7. O erro irá mencionar o aplicativo de 16 bits na janela de erro.</li>
<li>Se o jogo tiver um executável de 64 bits nativo, use-o também.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2,3 assinar arquivos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos os arquivos de código executáveis (por exemplo, extensões. exe e. dll) devem ser assinados com um certificado Authenticode. <br/> Se você estiver usando Windows Installer, os arquivos de pacote do instalador (arquivos. msi) deverão ser assinados. <br/></td>
</tr>
<tr class="even">

<td>Teste manual<br/>
<ol>
<li>Navegue até o diretório do jogo.</li>
<li>Localize todos os arquivos. exe e. dll.</li>
<li>Clique com o botão direito do mouse em Propriedades em cada arquivo.</li>
<li>Verifique se os arquivos executáveis do jogo contêm uma assinatura digital.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>Drivers de assinatura 2,4



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Qualquer driver de modo kernel instalado pelo jogo deve ser assinado com um certificado de Authenticode válido publicamente. <br/> Qualquer driver de dispositivo de hardware em modo kernel instalado pelo jogo deve ter uma assinatura da Microsoft obtida por meio do programa Windows Hardware Quality Labs (WHQL) ou Signature (assinatura de confiabilidade de driver). <br/></td>
</tr>
<tr class="even">

<td>Teste manual<br/>
<ol>
<li>Instale o jogo.</li>
<li>Verifique se o processo de instalação do jogo não exibe caixas de diálogo de driver não assinados.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2,5 executar verificação de versão corretamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Os jogos não devem falhar na execução em sistemas operacionais futuros, conforme indicado pelas alterações no número de versão do Windows, a menos que o contrato de licença de usuário final proíba o uso em sistemas operacionais futuros. Se o jogo for supostamente reprovado, ele deverá fazer isso normalmente exibindo uma mensagem ao usuário.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Instale o jogo no Windows XP, nas edições de 32 bits do Windows Vista e do Windows 7, e nas edições de 64 bits do Windows Vista e do Windows 7.</li>
<li>Verifique se o processo de instalação do jogo não encontrou um erro relacionado à versão do sistema operacional.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Teste automatizado</dt> <dd> Usar ferramenta: Application Verifier<br/>
<ol>
<li>Iniciar Application Verifier.</li>
<li>Habilite o teste Compatibility: HighVersionLie depois de selecionar o INSTALL.EXE.</li>
<li>Instale o jogo e verifique se ele não bloqueia a instalação com base na versão do sistema operacional.</li>
<li>Habilite o teste Compatibility: HighVersionLie depois de selecionar o GAME.EXE.</li>
<li>Execute o jogo e verifique se ele não bloqueia a execução com base na versão do sistema operacional.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2,6 suporte a sessões de usuário simultâneas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Os jogos devem oferecer suporte a cenários de multitarefa padrão do Windows.</td>
</tr>
<tr class="even">

<td>Crie uma conta de usuário padrão no Windows Vista ou no Windows 7 chamada Toby. Iniciar-> painel de controle-> adicionar ou remover contas de usuário-> criar nova conta <br/>
<ol>
<li>Inicie o jogo como o usuário Jane.</li>
<li>ALT + TAB de volta para a área de trabalho.</li>
<li>Verifique se o jogo ALT + TAB corretamente para a área de trabalho do Windows.</li>
<li>Clique em Iniciar-> [seta à direita de bloquear]-> Alternar usuário.</li>
<li>Faça logon como usuário Toby.</li>
<li>Verifique se o jogo é iniciado como usuário Toby enquanto ainda está sendo executado como o usuário Jane.</li>
<li>Verifique se o jogo não encontra erros para o usuário Toby ou o usuário Jane durante o processo de comutador do usuário.</li>
<li>Se você puder iniciar outra sessão de jogo, verifique se não consegue ouvir áudio da sessão de jogo original.</li>
<li>Feche o jogo e volte para o usuário e o jogo originais.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2,7 nomes longos de suporte



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Se um jogo oferecer suporte para salvar arquivos, ele deverá ser capaz de salvar arquivos que têm nomes e caminhos longos. O jogo deve lidar corretamente com caracteres especiais do sistema de arquivos, como//: *? &quot; < ou > em qualquer campo de entrada do usuário usado para criar caminhos ou nomes de arquivo.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie o jogo.</li>
<li>Inicie um novo jogo.</li>
<li>Salve o jogo. Durante o processo de salvamento, verifique se o jogo salva usando o nome para salvar: meu primeiro jogo salvo.</li>
<li>Saia de volta para o menu principal.</li>
<li>Tente carregar o jogo recentemente salvo.</li>
<li>Verifique se o jogo não encontra erros ao manipular caracteres de sistema de arquivos sem suporte, como \/: *? &quot; < ou > se o jogo lhe permitir, nomeie o jogo salvo.</li>
<li>Se o usuário tiver permissão para nomear seu perfil e/ou caractere ou salvar jogos, verifique se o jogo não encontra erros ao usar nomes de arquivo longos aqui também.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. instalação

### <a name="31-easy-install"></a>3,1 instalação fácil



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Jogos com uma instalação tradicional devem fornecer um caminho simplificado em sua interface de usuário de instalação.</td>
</tr>
<tr class="even">

<td><ol>
<li>Insira o disco do jogo.</li>
<li>Verifique se o jogo não exibe mais de um contrato de licença de End-User (EULA).</li>
<li>Se o jogo oferecer suporte a uma opção de instalação personalizada ou avançada, verifique se essa opção pode ser acessada durante o processo de instalação.</li>
<li>Verifique se a opção de instalação padrão ignora todas as seleções de entrada de usuário para o processo de instalação (seleção de pasta de instalação, seleção de componentes e assim por diante).</li>
<li>Verifique se o processo de instalação do jogo não solicita a configuração do componente do so (instalação do DirectX, tempos de execução do Visual C e assim por diante).</li>
<li>Verifique se o processo de instalação do jogo não solicita a interação do firewall.</li>
<li>Verifique se o jogo é executado automaticamente ou se um menu do inicializador está presente no final do processo de instalação.</li>
<li>Verifique se o processo de desinstalação do jogo remove todos os arquivos de componente do sistema operacional instalados e não redistribuídos e limpa todas as configurações. A limpeza de todas as configurações por usuário e os dados (como jogos salvos) não é necessário.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3,2 controle de conta de usuário de suporte para instalação



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>O instalador de jogos não deve presumir que está sendo executado no mesmo contexto que o usuário. Os jogos devem, portanto, executar tarefas por usuário na primeira execução separadamente da instalação.</td>
</tr>
<tr class="even">

<td><ol>
<li>Verifique se você pode instalar o jogo como o usuário Jane. (Isso exigirá direitos elevados durante o processo de instalação/instalação.)</li>
<li>Verifique se o processo de instalação do jogo solicita ao usuário Jane a elevação por meio de credenciais de administrador. (A solicitação para elevar será exibida quando o usuário tentar instalar.)</li>
<li>Opte por executar automaticamente o jogo no final da instalação, se ele ainda não fizer isso, ou inicie-o no menu que aparece.</li>
<li>Após o jogo, crie um novo perfil, Jogue e salve um jogo.</li>
<li>Saia do jogo.</li>
<li>Reinicie o jogo e verifique se os perfis de usuário e os jogos salvos podem ser acessados pela conta Jane do usuário.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3,3 instalar em pastas corretas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Os jogos devem ser instalados na pasta arquivos de programas por padrão. Os dados do usuário devem ser gravados na primeira execução e não durante a instalação.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale o jogo usando o tipo de instalação padrão.</li>
<li>Verifique se o jogo foi instalado em arquivos de programas.</li>
</ol>
<blockquote>
[!Note]<br />
Se esse teste falhar, verifique se o jogo destina-se a instalar para todos os usuários. Nesse caso, isso é uma falha.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3,4 instalar recursos do Windows corretamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Os aplicativos não devem tentar instalar arquivos ou chaves do registro protegidos por Proteção de Recursos do Windows (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>Verifique se nenhuma caixa de diálogo Proteção de Recursos do Windows WRP aparece durante o processo de instalação.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitar reinicializações durante a instalação



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>O instalador de jogos não deve supor que a instalação de componentes do Windows a partir de pacotes de redistribuição exige uma reinicialização, a menos que a reinicialização seja indicada por um resultado de retorno ou pela documentação da Microsoft.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale o jogo.</li>
<li>Verifique se o jogo não exige que o sistema seja reinicializado após a instalação.</li>
</ol>
<blockquote>
[!Note]<br />
Se um Redist de atualização de sistema da Microsoft exigir uma reinicialização, faça o seguinte: conclua a instalação do jogo, desinstale o jogo e reinstale o jogo uma segunda vez. O processo de instalação do jogo não deve exigir uma reinicialização nesta segunda instalação.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3,6 usar o controle de versão de arquivo corretamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>O programa de instalação de jogos deve verificar corretamente se as versões de arquivo mais recentes estão instaladas. Instalar um jogo nunca deve retornar nenhum arquivo que você não produz ou que são compartilhados por aplicativos que você não produz.</td>
</tr>
<tr class="even">

<td><ol>
<li>Antes de instalar o jogo, crie um instantâneo de pré-instalação de system32.<br/>
<ol>
<li>Crie um diretório chamado G4Wtest.</li>
<li>Abra uma janela de comando (Start-> execute-> cmd).</li>
<li>Navegue até c:\Windows\System32.</li>
<li>Digite dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Crie um instantâneo pós-instalação de system32. <br/>
<ol>
<li>Abra uma janela de comando (Start-> execute-> cmd).</li>
<li>Navegue até c:\Windows\System32.</li>
<li>Digite dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</li>
<li>Verifique se o jogo não retorna nenhuma versão de arquivo dos arquivos que o jogo não produziu (... dos arquivos listados nos dois documentos, comparando pregame.txt a postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3,7 suporte a \[ requisito condicional de Autorun\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Para jogos distribuídos em CD, DVD ou outras mídias removíveis que oferecem suporte a autorun, quando o disco é inserido pela primeira vez, o aplicativo deve executar automaticamente ou solicitar que o usuário instale o jogo. <br/>
<blockquote>
[!Note]<br />
Os programas autorun que foram escritos para uso em versões do Windows anteriores ao Windows Vista não devem usar o tempo de execução do .NET, pois essa tecnologia não está incluída no Windows XP ou em versões anteriores do Windows.
</blockquote>
<br/> Para obter mais diretrizes, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">jogos para requisitos técnicos do Windows</a> 3,7, suporte a autorun. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Insira o disco ou a mídia do jogo.</li>
<li>Verifique se a caixa de diálogo instalar/executar é exibida automaticamente.</li>
<li>Windows Vista ou Windows 7: Verifique se o programa Autorun do jogo em si não solicita ao usuário Jane para elevar por meio de credenciais de administrador.</li>
<li>Verifique se o executável de Autorun não precisa de componentes de redistribuição prontos para uso, como .NET 3,5, C Run-Time Libraries e assim por diante.</li>
<li>Verifique se a reinserção do disco na unidade após a instalação não faz com que a instalação seja iniciada automaticamente.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. confiabilidade

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminar reinicializações desnecessárias



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Todos os instaladores de aplicativo devem aproveitar as APIs do Gerenciador de reinicialização para evitar reinicializações do sistema (consulte o [requisito 3,5](#35-avoid-reboots-during-installation)). |



 

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminar falhas de Application Verifier



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>O jogo deve gerar nenhuma falha em execução no Microsoft Application Verifier (AppVerifier), versão 4,0 ou posterior, nos seguintes testes: <br/>
<ul>
<li>Noções básicas: identificadores, heaps, bloqueios, memória, TLS</li>
<li>Diversos: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Usar ferramenta: AppVerifier 4,0 (ou posterior)<br/>
<ol>
<li>Instale o AppVerifier.</li>
<li>Inicie o AppVerifier e selecione Arquivo-> Adicionar aplicativo.</li>
<li>Localize o executável do jogo, selecione-o e clique &quot; no &quot; botão abrir.</li>
<li>Na &quot; seção aplicativos &quot; , selecione o executável do jogo.</li>
<li>Na &quot; seção testes &quot; , selecione os testes listados acima em &quot; noções básicas de categorias &quot; e &quot; diversos &quot; (desmarque ThreadPool e sobreposição) e verifique se todos os outros testes não estão selecionados.</li>
<li>Inicie o jogo.</li>
<li>Verifique se o jogo não gera falhas quando executado em Application Verifier.</li>
</ol>
<blockquote>
[!Note]<br />
Alguns testes exigem que um depurador seja totalmente executado. Isso pode exigir uma versão de lançamento desprotegida do executável do jogo, uma vez que a tecnologia antifalsificação/antipirataria pode interferir no AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>suporte a 4,3 Relatório de Erros do Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Os jogos devem tratar apenas as exceções conhecidas e esperadas e Relatório de Erros do Windows não devem ser desabilitadas. Se uma falha (como uma violação de acesso) for injetada em um jogo, ela deverá permitir que Relatório de Erros do Windows relate a falha.</td>
</tr>
<tr class="even">

<td>Ferramenta de uso: seqüestrador de thread <br/>
<ul>
<li>Se o aplicativo falhar durante o teste, verifique se o jogo exibe Relatório de Erros do Windows corretamente e coleta dados de falha.</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos os arquivos executáveis (por exemplo, arquivos. exe ou. dll) devem conter um nome de produto preciso, nome da empresa e versão do arquivo.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Teste manual:</dt> <dd>
<ol>
<li>Clique com o botão direito do mouse nos arquivos executáveis do jogo na mídia de instalação e aqueles instalados no disco rígido do computador.</li>
<li>Selecione Propriedades.</li>
<li>Windows XP: clique na guia <strong>versão</strong> . Verifique se os campos nome do produto, nome da empresa e versão do arquivo estão populados corretamente.</li>
<li>Windows Vista ou Windows 7: clique na guia <strong>detalhes</strong> . Verifique se os campos nome do produto e versão do arquivo estão populados corretamente. O nome da empresa não está visível na página de propriedades do Windows Vista ou do Windows 7.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Teste automatizado:</dt> <dd>
<ul>
<li>Use a ferramenta de teste Microsoft Games para Windows; consulte a <a href="#64-microsoft-games-for-windows-test-tool">seção 6,4</a>.</li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>A saída normal do jogo não deve resultar em uma falha de exceção desconhecida.</td>
</tr>
<tr class="even">

<td><ul>
<li>Depois de jogar o jogo para uma sessão normal de jogos, verifique se o jogo não gera erros na saída.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. exemplo de script de teste

Este é um exemplo de uma etapa de teste típica usando os requisitos de teste anteriores como guia.

### <a name="51-tools"></a>ferramentas de 5,1

-   edição de 32 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU AMD
-   edição de 32 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU Intel
-   edição de 64 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU AMD
-   edição de 64 bits do Windows Vista SP1 e/ou Windows 7 em uma CPU Intel
-   edição de 32 bits Windows XP SP2 em uma CPU AMD
-   edição de 32 bits Windows XP SP2 em uma CPU Intel
-   Monitor de tela larga que dá suporte a 1680 1050
-   Controlador Xbox 360 para Windows

### <a name="52-pre-install"></a>5,2 pré-instalação

1.  Windows Vista e Windows 7: criar dois usuários padrão: Jane e Toby
2.  Windows Vista e Windows 7: Verifique se o controle de conta de usuário está habilitado
3.  Criar um instantâneo de pré-instalação de system32

    1.  Crie um diretório chamado G4Wtest
    2.  Exibir uma janela de comando (Start-> execute-> cmd)
    3.  Navegue até c: \\ Windows \\ System32
    4.  Digite dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista e Windows 7: definido como 150% DPI \[ 1,8\]
5.  Continuar a [instalação](#3-installation)

### <a name="53-install"></a>instalação do 5,3

1.  Fazer logon como usuário Jane
2.  Insira o disco do jogo na unidade de CD/DVD, verifique se a caixa de diálogo instalar/executar é exibida automaticamente \[ 3,7\]
3.  Verifique se o processo de instalação do jogo solicita ao usuário Jane para elevar as credenciais de administrador \[ 3,2\]
4.  Verifique se o programa Autorun do jogo em si não solicita ao usuário Jane para elevar as credenciais de administrador \[ 3,7\]
5.  Verifique se o jogo não exibe mais de um contrato de licença de End-User (EULA) \[ 3,1\]
6.  Verifique se o jogo exibe as opções de instalação padrão/fácil e personalizada/avançada \[ 3,1\]
7.  Verifique se a opção de instalação padrão/fácil ignora todas as seleções de entrada de usuário para o processo de instalação (seleção de pasta de instalação, seleção de componentes e assim por diante) \[ . 3,1\]
8.  Verifique se o processo de instalação do jogo não solicita a instalação do componente do so (instalação do DirectX, bibliotecas de Run-Time do C e assim por diante) \[ . 3,1\]
9.  Verifique se o processo de instalação do jogo não solicita a interação do firewall \[ 3,1\]
10. Verifique se o processo de instalação do jogo não encontrou um erro relacionado ao sistema operacional versão \[ 2,5 \] \[ 4,2\]
11. Verifique se o processo de instalação do jogo não exibe caixas de diálogo (s) de driver não assinado \[ 2,4\]
12. Verifique se nenhuma caixa de diálogo Proteção de Recursos do Windows (WRP) aparece durante o processo de instalação \[ 3,4\]
13. Verifique se inserindo novamente o disco na unidade após a instalação não faz com que a instalação seja iniciada automaticamente
14. Verifique se o jogo não exige que o sistema seja reinicializado após a instalação \[ 3,5\]
15. Verifique se você pode instalar o jogo como o usuário Jane \[ 3,2\]
16. Verifique se o jogo é executado automaticamente ou se um menu do inicializador está presente no final do processo de instalação \[ 3,1\]
17. Se o jogo executar automaticamente após a instalação, pule para [tempo de execução](#55-runtime)
18. Se o jogo deixasse um menu de inicialização para cima ou falhou ao desinstalar, consulte [a seção pós-instalação](#54-post-install)

### <a name="54-post-install"></a>5,4 pós-instalação

1.  Verifique se o jogo não coloca os atalhos de inicialização no usuário área de trabalho \[ 1,1\]
2.  Verifique se o jogo não coloca os atalhos de inicialização no menu iniciar \[ 1,1\]
3.  Verifique se o ícone de jogo é exibido no explorador de jogos do Windows \[ 1,1\]
4.  Verifique se os metadados (Publicador, desenvolvedor, gênero, data de lançamento, versão) na parte inferior são exibidos e estão corretos \[ 1,1\]
5.  Verifique se o ícone de jogo exibe informações do WEI (índice de experiência do Windows) no explorador de jogos do Windows \[ 1,1\]
6.  Verifique se os hiperlinks de jogos para os metadados funcionam corretamente no explorador de jogos do Windows \[ 1,1\]
7.  Verifique se o jogo exibe a classificação de controle dos pais preciso no explorador de jogos do Windows \[ 1,1\]
8.  Criar um instantâneo pós-instalação de system32

    1.  Exibir uma janela de comando (Start-> execute-> cmd)
    2.  Navegue até c: \\ Windows \\ System32
    3.  Digite dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Verifique se o jogo não retorna nenhuma versão de arquivo dos arquivos listados nos dois documentos, comparando pregame.txt a postgame.txt \[ 3,6\]

9.  Continuar em [tempo de execução](#55-runtime)

### <a name="55-runtime"></a>5,5 tempo de execução

1.  TEMPO de execução 1: se o menu iniciar estiver presente, inicie o jogo a partir daí. Se o jogo for executado automaticamente ou tiver sido iniciado no menu do inicializador de jogos após a instalação, execute o seguinte: caso contrário, pule para o tempo de execução 2:

    1.  Criar um perfil (se o jogo permitir)
    2.  Iniciar um novo jogo
    3.  Salvar o jogo
    4.  Sair do jogo
    5.  Iniciar o jogo no explorador de jogos
    6.  Verifique se o jogo é iniciado no ícone do explorador de jogos \[ 1,2\]
    7.  Verifique se o jogo não solicita credenciais de administrador na inicialização \[ 1,2\]
    8.  Verifique se os perfis de usuário e os jogos salvos podem ser acessados pelo usuário Carina conta \[ 3,2\]
    9.  Prosseguir para o tempo de execução 3

2.  TEMPO de execução 2: se o jogo não executar automaticamente ou exibir uma inicialização no menu do inicializador de jogos, isso é uma falha de \[ 3,1 \] ; no entanto, o teste pode continuar normalmente:

    1.  Iniciar o jogo no explorador de jogos
    2.  Verifique se o jogo é iniciado no ícone do explorador de jogos \[ 1,2\]
    3.  Verifique se o jogo não solicita credenciais de administrador na inicialização \[ 1,2\]
    4.  Prosseguir para o tempo de execução 3

3.  TEMPO de execução 3: se o jogo der suporte a um game pad, verifique se o jogo reconhece o controlador Xbox 360 para Windows como um dispositivo de entrada \[ 1,4\]

    1.  Se necessário, habilite o controlador por meio do menu de opções
    2.  Verifique se o jogo refere-se aos botões e gatilhos do controlador usando os nomes do Xbox 360
    3.  Verifique se o jogo e o sistema de menus são controláveis com o controlador Xbox 360 para Windows
    4.  Verifique se o controlador Xbox 360 para Windows se comporta de acordo com os padrões aceitos

4.  Defina o vídeo como \[ 1,5 \] :

    1.  Verifique se o jogo é executado a uma resolução de proporção de 4:3 (800 600 ou 1024 768)
    2.  Verifique se o jogo é executado a uma resolução de proporção de 16:9 (1280 720)
    3.  Verifique se o jogo é executado a uma resolução de proporção de 16:10 (1680 1050, 800 480 ou 1152 720)
    4.  Verifique se o jogo solicita o usuário quando uma alteração é feita na resolução
    5.  Verifique se a exibição é revertida para a configuração anterior se você não aceitar dentro de 15 segundos
    6.  Verifique se o jogo não amplia a imagem e, por sua vez, apresenta uma área mais ampla de exibição
    7.  Verifique se o jogo não adiciona barras pretas à esquerda e à direita da área de jogo

5.  Se estiver disponível nas configurações de vídeo, verifique se as opções de processamento do jogo são padrão para Direct3D \[ 1,7 \] ; caso contrário, prossiga para [testes automatizados](#58-automated-tests)
6.  Se solicitado ou se a opção estiver disponível, crie um perfil de usuário. Verifique se o jogo não encontrou erros ao usar nomes de arquivo longos \[ 2,7\]
7.  Inicie um novo jogo, crie um jogo e verifique se o jogo não encontrou erros ao manipular os caracteres do sistema de arquivos sem suporte \[ 2,7\]
8.  Verifique se o jogo ALT + TAB corretamente para a área de trabalho do Windows \[ 2,6\]

    1.  Alterne os usuários com o jogo em execução clicando em Iniciar-> Alternar usuário
    2.  Fazer logon como Toby
    3.  Verifique se o jogo é iniciado como usuário Toby enquanto ainda está em execução como usuário Jane \[ 2,6\]
    4.  Verifique se o jogo não encontra erros para o usuário Toby ou o usuário Jane durante o processo de mudança de usuário \[ 2,6\]
    5.  Verifique se você não consegue ouvir áudio da sessão de jogo original \[ 2,6\]
    6.  Sair do jogo
    7.  Fazer logoff de Toby
    8.  Voltar para o usuário original onde o jogo está em execução
    9.  ALT + TAB de volta ao jogo

9.  Sair do jogo
10. Prosseguir para o [pós-tempo de execução](#56-post-runtime)

### <a name="56-post-runtime"></a>5,6 pós-tempo de execução

1.  Verifique se o jogo não gera erros na saída \[ 4,3\]
2.  Verifique se o jogo instalado nos arquivos de programas \[ 3,3\]
3.  Ir para os [controles dos pais](/windows)

### <a name="57-parental-controls"></a>5,7 controles dos pais

1.  Abrir controles dos pais no painel de controle
2.  Verifique se o jogo exibe a classificação de controle dos pais preciso abaixo do título do jogo no painel de controle dos controles dos pais \[ 1,2\]
3.  Consulte o caso de teste \[ 1,2 \] para os seguintes testes:

    1.  Depois de definir os controles dos pais como "on", verifique se o jogo é executado com essas configurações como o usuário Jane \[ 1,2\]
    2.  Fazer logoff e logon como Toby
    3.  Verifique se o jogo é executado com essas configurações como usuário Toby \[ 1,2\]
    4.  Fazer logoff e logon como Jane
    5.  Na seção controle dos pais, bloqueie o usuário Toby de ver jogos um nível ESRB e superior do jogo que você acabou de instalar

        Exemplo: se o jogo for classificado como E, defina-o para que Toby possa reproduzir jogos classificados como C

    6.  Verifique se o jogo é executado com essas configurações como o usuário Jane \[ 1,2\]
    7.  Fazer logoff e logon como usuário Toby
    8.  Verifique se o jogo não é iniciado no usuário Toby quando ESRB está bloqueado pelo usuário Jane \[ 1,2\]
    9.  Fazer logoff como usuário Toby e voltar como usuário Jane
    10. Se alterado anteriormente, restaure as configurações de ESRB
    11. Se não houver configurações de ESRB, selecione "bloquear ou permitir jogos específicos" e selecione o jogo por nome
    12. Fazer logoff como Jane e on as Toby
    13. Verifique se o jogo não é iniciado no usuário Toby quando o EXE/Name está bloqueado pelo usuário Jane \[ 1,2\]
    14. Fazer logoff como Toby e voltar como Jane
    15. Como Jane, abra controles de usuário-> restrições de aplicativo
    16. Clique em "Toby pode usar apenas os programas que eu permitir" e, em seguida, clique em OK (ou seja, não permitir nenhum EXEs)
    17. Clique na caixa desmarcar tudo e, em seguida, clique em OK
    18. Ir para controles de usuários controles de \| jogos e permitir o jogo específico usando a classificação ESRB
    19. Faça logoff como Jane e faça logon como Toby e tente jogar o jogo
    20. Verifique se o jogo não está bloqueado e se o Toby pode reproduzi-lo quando "permitir nenhum EXEs" estiver definido \[ 1,2\]
    21. Fazer logoff como usuário Toby e voltar como usuário Jane
    22. Vá para controles dos pais no painel de controle e remova as restrições
    23. Verifique se os dois usuários podem agora jogar o jogo

4.  Prosseguir para os [testes automatizados](#58-automated-tests)

### <a name="58-automated-tests"></a>5,8 testes automatizados

1.  Verifique se o jogo não gera falhas quando executado em Application Verifier-consulte a documentação da ferramenta de teste de identidade visual \[ 4,2\]
2.  Verifique se os arquivos executáveis do jogo contêm manifestos-consulte a documentação da ferramenta de teste de identidade visual \[ 2,1\]
3.  Verifique se o manifesto do arquivo executável do jogo requestedExecutionLevel é "AsInvoker"-consulte a documentação da ferramenta de teste de identidade visual \[ 2,1\]
4.  Prosseguir para [outros testes](#59-other-tests)

### <a name="59-other-tests"></a>5,9 outros testes

1.  Verifique se os arquivos executáveis do jogo contêm uma assinatura digital \[ 2,3\]
2.  Verifique se o processo de instalação do jogo é executado normalmente em edições de 64 bits do Windows Vista e/ou do Windows 7 \[ 2,3\]
3.  Verifique se o jogo não encontrou um erro como resultado de executáveis de 16 bits em edições de 64 bits do Windows Vista e/ou do Windows 7 \[ 2,3\]
4.  Forçar o aplicativo a falhar durante o teste e verificar se o jogo exibe Relatório de Erros do Windows corretamente e coleta os dados de falha \[ 4,3\]
5.  Garantir resumos de arquivos apropriados \[ 4,3\]

    1.  Clique em Iniciar-> computador
    2.  Navegue até o diretório do jogo
    3.  Na janela de pesquisa, digite \* . dll
    4.  Para cada arquivo: clique com o botão direito do mouse no arquivo e clique em Propriedades

        -   No Windows XP: clique na guia versão. Verifique se os campos nome do produto, nome da empresa e versão do arquivo estão populados corretamente. \[4.3\]
        -   No Windows Vista e no Windows 7: clique na guia detalhes. Verifique se os campos nome do produto e versão do arquivo estão populados corretamente. O nome da empresa não está visível na página de propriedades do Windows Vista ou do Windows 7 \[ 4,3\]

    5.  Repita essa verificação para arquivos. exe

6.  Inicie o jogo.

    1.  Pressione CTRL + ALT + DEL
    2.  Clique na seta "opções de desligamento"
    3.  Clique em reiniciar
    4.  Verificar se o jogo não bloqueia o desligamento \[ 3,1\]

7.  Continuar a [desinstalação](#510-uninstall)

### <a name="510-uninstall"></a>5,10 desinstalar

-   Verifique se o processo de desinstalação do jogo remove todos os arquivos de componente do sistema operacional instalados e não redistribuídos e limpa todas as configurações \[ 3,1\]

    -   Verifique no Windows Vista ou no Windows 7 se o painel de controle é a única maneira de remover o programa \[ 1,1\]

## <a name="test-tool-notes"></a>Notas da ferramenta de teste

Estas são observações para cada uma das ferramentas de teste listadas nos requisitos de teste acima.

### <a name="61-appverifier-40-or-higher"></a>6,1 AppVerifier 4,0 (ou superior)

**Caso de teste: 2,5, 4,2**

> [!Note]  
> Alguns aplicativos falham ao serem executados com o AppVerifier em execução, devido à proteção de cópia. Isso pode ser resolvido executando com uma versão de lançamento desprotegida do executável do jogo.

 

1.  Instalar o AppVerifier 4,0 (ou superior) em um computador que executa o Windows XP
2.  Inicie o AppVerifier e clique em arquivo-> Adicionar aplicativo
3.  Localize o executável do jogo, selecione-o e clique em abrir
4.  Na seção "aplicativos", selecione o executável do jogo
5.  Selecione os seguintes testes na seção "Noções básicas":

    -   Alças
    -   Heaps
    -   Locks
    -   Memória
    -   TLS

6.  Selecione os seguintes testes na seção "diversos":

    -   DangerousAPIs
    -   DirtyStacks

7.  Verifique se todos os outros testes não estão selecionados
8.  Iniciar o jogo
9.  Jogue o jogo
10. Fechar o jogo
11. Em AppVerifier, selecione Exibir-> logs
12. Na seção "aplicativos", selecione o arquivo app. exe
13. Na seção "logs", selecione o arquivo de log e observe a contagem de erros. Se não houver erros, encerre os testes do AppVerifier. Se houver erros, clique no botão exibir
14. Pesquisar o documento (CTRL + F) para severidade = "erro
15. Criar bugs com base na parte da Camadaname = da falha

### <a name="62-manifest-test---mtexe"></a>Teste de manifesto 6,2-mt.exe

**Caso de teste: 1,8, 2,1**

Essa ferramenta é executada em um prompt de comando onde MT.exe está localizado.

Exemplo:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Clique em Iniciar-> executar-> digite cmd e clique no botão OK
2.  Execute a ferramenta de mt.exe para gerar um arquivo. manifest para cada arquivo. exe que é instalado com o jogo
3.  Abrir o arquivo. manifest gerado
4.  Verifique se cada arquivo. exe contém o seguinte (solicitado:

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> O nível de execução solicitado deve estar presente para cada arquivo e dpiAware deve estar presente para pelo menos o arquivo executável do jogo s.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6,3 de thread seqüestrador-threadhijacker.exe

Essa ferramenta é executada em um prompt de comando onde threadhijacker.exe está localizado.

Exemplo:

``` syntax
threadhijacker.exe /process:str
```

Em que Str é o nome \_ do \_program.exe

1.  Ative o Gerenciador de tarefas, clique na guia processos e localize o nome do executável do jogo.
2.  Abrir um prompt de comando no modo de administrador
3.  Navegue até o diretório onde threadhijacker.exe está
4.  Tipo: **threadhijacker.exe/Process:** Str, em que Str é o nome do executável que você deseja atingir

### <a name="64-microsoft-games-for-windows-test-tool"></a>6,4 Microsoft Games para Windows Test Tool

Essa ferramenta está localizada no SDK do DirectX. Depois que o SDK é instalado em um computador, o instalador da ferramenta de teste jogos para Windows pode ser colocado no computador de teste e instalado.

Localize o instalador da ferramenta de teste do Microsoft Games para Windows no computador de desenvolvimento em que o SDK do DirectX está instalado. Por padrão, ele é colocado no seguinte local:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copie o instalador (MicrosoftGFWTestTool.msi/setup.exe) para o computador de teste.
2.  Execute o instalador.
3.  Inicie a ferramenta de teste Microsoft Games para Windows.
4.  No campo **lista de projetos** , substitua **criar novo projeto** pelo nome do título e clique em **criar novo**.

    Aguarde a conclusão da linha de base.

5.  Preencha todas as informações que você possa ter na seção **informações do jogo** e clique em **Atualizar informações do jogo**.
6.  Clique na guia **casos de teste** .
7.  Começando na parte superior, prossiga com os casos de teste, clicando em **passar** ou **falhar** conforme apropriado.

    Consulte "escrevendo um bug", mais adiante nesta seção, para obter detalhes sobre como incluir um bug no relatório.

8.  Retorne à guia **projetos** depois de revisar o relatório (marcando as guias **relatório** e **edição de bug** ).
9.  Clique em **Compilar relatório**.

    Uma janela será aberta quando o relatório terminar a compilação. Aqui, você encontrará um. Os nomes de arquivo ZIPreport.zip *ProjectName* \_ . Esse arquivo contém todos os logs e resultados coletados durante a fase de teste.

### <a name="writing-a-bug"></a>Escrevendo um bug

Há duas maneiras de escrever um relatório de bugs: você pode percorrer os casos de teste e clicar em **falha** quando o título falha em um caso de teste, ou você pode clicar na guia **edição de bug** e adicionar manualmente um relatório de bug.

### <a name="clicking-fail-on-a-test-case"></a>Clicando em falha em um caso de teste

1.  Quando você clica em **falha** em um caso de teste, a lista suspensa **tipo de problema** será automaticamente definida como o tipo de caso de teste.
2.  Adicione uma breve descrição ao campo **título** que descreve brevemente o problema.
3.  Adicione uma descrição detalhada do problema ao campo **comportamento observado** .
4.  Conforme apropriado, adicione o que era esperado (em oposição a uma descrição do problema) ao campo de **comportamento esperado** .
5.  Adicione uma descrição detalhada de como reproduzir o problema para o campo de **etapas de reprodução** .
6.  Quando terminar, clique no botão **salvar** .

### <a name="manually-adding-a-bug"></a>Adicionando um bug manualmente

Esse processo é o mesmo que clicar em **falha**, com exceção da lista suspensa preenchida automaticamente. Nesse caso, selecione o tipo de falha TCR apropriado ou selecione **\* \* problema \* \* não-TR** para bugs que estão fora do intervalo de TR, mas que ainda devem ser relatados.

## <a name="resources"></a>Recursos

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Jogos para Windows: requisitos técnicos
</dt> <dd>

[Jogos para requisitos técnicos do Windows: práticas recomendadas para jogos no Windows XP, Windows Vista e Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>SDK do Windows
</dt> <dd>

[SDKs do Windows](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Diretrizes de controle de conta de usuário
</dt> <dd>

[Requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Informações de Windows Installer
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portal do desenvolvedor do WinQual 
</dt> <dd>

[Winqual (Windows Quality Online Services)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portal do desenvolvedor do DirectX
</dt> <dd>

[Central de desenvolvedores do DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de jogos para Windows e SDK do DirectX
</dt> <dd>

[Jogos para Windows e SDK do DirectX](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artigos adicionais sobre o DirectX
</dt> <dd>

[Artigos técnicos sobre o DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

