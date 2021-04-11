---
description: A partir do Windows 8, o SDK do DirectX é incluído como parte do SDK do Windows.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Onde está o SDK do DirectX?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd863bf29858f2313641aca161c73754b789015c
ms.sourcegitcommit: b4beb606419fea6a256b8332a9ea930607e60612
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103930264"
---
# <a name="where-is-the-directx-sdk"></a>Onde está o SDK do DirectX?

A partir do Windows 8, o SDK do DirectX é incluído como parte do SDK do Windows.

Criamos originalmente o SDK do DirectX como uma plataforma de alto desempenho para desenvolvimento de jogos sobre o Windows. À medida que as tecnologias do DirectX amadureceram, elas se tornaram relevantes para uma gama mais ampla de aplicativos. Hoje, a disponibilidade do hardware de Direct3D em computadores impulsiona os aplicativos de área de trabalho tradicionais para usar aceleração de hardware de gráficos. Em paralelo, as tecnologias do DirectX são mais integradas ao Windows. O DirectX agora é uma parte fundamental do Windows.

Como o SDK do Windows é o principal SDK do desenvolvedor para Windows, o DirectX agora está incluído nele. Agora você pode usar o SDK do Windows para criar jogos incríveis para o Windows. Para baixar o SDK do Windows 8. x ou o SDK do Windows 10, consulte [SDK do Windows e arquivo de emulador](https://developer.microsoft.com/windows/downloads/sdk-archive).

As tecnologias e ferramentas a seguir, anteriormente parte do SDK do DirectX, agora fazem parte do SDK do Windows.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnologia ou ferramenta</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Componentes gráficos do Windows<br/></td>
<td>Os cabeçalhos e as bibliotecas para <a href="/windows/desktop/direct3d">Direct3D</a> e outras APIs de gráficos do Windows, como <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, estão disponíveis no SDK do Windows. <br/>
<blockquote>
[!Note]<br />
As bibliotecas do utilitário preterido D3DX9/D3DX10/D3DX11 estão disponíveis por meio do <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, mas também há uma série de <a href="https://walbourn.github.io/living-without-d3dx/">alternativas de código aberto</a>. A biblioteca do utilitário D3DCSX DirectCompute e a DLL redistribuível estão disponíveis no SDK do Windows. D3DX12 está disponível no <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilador HLSL (FXC.EXE)<br/></td>
<td>O compilador <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> é uma ferramenta no subdiretório de arquitetura apropriado na pasta bin do SDK do Windows.<br/>
<blockquote>
[!Note]<br />
A API D3DCompiler e a DLL redistribuível estão disponíveis no SDK do Windows.
</blockquote>
<br/><br/>Para o desenvolvimento do DirectX 12, use o DXCompiler no SDK do Windows e hospedado no [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX para Windows<br/></td>
<td>Uma substituição para a ferramenta PIX para Windows agora é um recurso no Microsoft Visual Studio, chamado depurador de gráficos do Visual Studio. Esse recurso melhorou muito a usabilidade, o suporte para o Windows 8 e o Direct3D 11,1 e a integração com recursos tradicionais de Microsoft Visual Studio, como pilhas de chamadas e janelas de depuração para depuração <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Para obter mais informações sobre esse novo recurso, consulte <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">depuração de elementos gráficos do DirectX</a>.<br/><br/>Para o desenvolvimento do DirectX 12, consulte a última geração de <a href="https://devblogs.microsoft.com/pix/">PIX no Windows</a><br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> para Windows<br/></td>
<td>A API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> agora é um componente de sistema no Windows 8. x e Windows 10. Os cabeçalhos e as bibliotecas para XAudio2 estão disponíveis no SDK do Windows. Para obter suporte para o Windows 7, consulte <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> para Windows<br/></td>
<td>A API do <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 agora é um componente do sistema no Windows 8. x e Windows 10. Os cabeçalhos e as bibliotecas para XInput estão disponíveis no SDK do Windows.<br/>
<blockquote>
[!Note]<br />
O XInput 9.1.0 herdado também está disponível como parte do Windows 7 ou posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br/></td>
<td>A versão mais recente do XNAMATH, que é atualizada para novos conjuntos de instruções, bem como ARM/ARM64, agora é <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. Os cabeçalhos para DirectXMath estão disponíveis no SDK do Windows e no <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Painel de controle do DirectX e visualizador de recursos do DirectX<br/></td>
<td>Os utilitários do painel de controle do DirectX e do Visualizador de recursos do DirectX estão incluídos no subdiretório de arquitetura apropriado na pasta bin do SDK do Windows. O Visualizador de recursos do DirectX também está disponível no <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACTSET<br/></td>
<td>A ferramenta de multiplataforma de áudio Xbox (transação) não tem mais suporte para uso no Windows.<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de jogos</a> e GDFMAKER<br/></td>
<td>A API do <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de jogos</a> apresenta jogos para os usuários do Windows. A API do explorador de jogos tem suporte apenas no Windows Vista e no Windows 7. Use a ferramenta criador de arquivos de definição de jogos (GDFMAKER.EXE) para declarar classificações de jogos para aplicativos da Windows Store. <br/> A ferramenta criador de arquivos de definição de jogos (GDFMaker.exe) está incluída no subdiretório x86 sob a pasta bin na SDK do Windows e dá suporte a aplicativos da Windows Store e de área de trabalho do Win32.<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Exemplos<br/></td>
<td>Você pode encontrar aplicativos de exemplo que realçam as tecnologias DirectX 12 no Windows no repositório de <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">exemplos do DirectX</a> . A maioria dos exemplos de versões mais antigas do Direct3D também está disponível online. Para obter mais informações sobre esses exemplos, consulte <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catálogo de exemplos do SDK do DirectX</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 gerenciado<br/></td>
<td>Os assemblies do .NET DirectX são preteridos e não são recomendados para uso por novos aplicativos. Há várias alternativas disponíveis. Consulte <a href="https://walbourn.github.io/directx-and-net/">DirectX e .net</a>. <br/></td>
</tr>
</tbody>
</table>



 

O SDK do DirectX herdado está disponível para download no [centro de download da Microsoft](http://go.microsoft.com/fwlink/?LinkId=226640) , se necessário, mas o uso para novos projetos não é recomendado.

> [!Note]  
> O SDK do DirectX não será instalado se você tiver uma determinada versão do pacote redistribuível do Visual C++ 2010 já instalado. Para obter mais informações sobre o e uma solução para corrigir esse problema, consulte [o erro "S1023" ao instalar o SDK do DirectX (junho de 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Usando projetos SDK do DirectX com o Visual Studio

Os exemplos do SDK do DirectX de junho de 2010 têm suporte com SKUs Premium do Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 ou Microsoft Visual Studio Ultimate 2013) no Windows 7 e no Windows 8 e versões posteriores. Devido à transição de cabeçalhos e bibliotecas do DirectX para o SDK do Windows, as alterações nas configurações do projeto são necessárias para criar esses exemplos corretamente com o modo como o SDK do Windows 8 e posterior é empacotado com os SKUs Premium do Visual Studio.

Essas etapas também se aplicam aos seus próprios projetos que dependem do SDK do DirectX.

1.  Verifique se a versão de junho de 2010 do SDK do DirectX está instalada no seu computador de desenvolvimento. Se você instalar o em um computador que executa o Windows 8 e posterior, será solicitado e necessário habilitar o .NET 3,5 como uma instalação de pré-requisito para o SDK do DirectX.

    > [!Note]  
    > O SDK do DirectX não será instalado se você tiver uma determinada versão do pacote redistribuível do Visual C++ 2010 já instalado. Para obter mais informações sobre o e uma solução para corrigir esse problema, consulte [o erro "S1023" ao instalar o SDK do DirectX (junho de 2010)](https://support.microsoft.com/kb/2728613).

     

2.  Verifique se você está usando uma das SKUs Premium do Visual Studio. Microsoft Visual Studio Express 2012 para Windows 8 ou Microsoft Visual Studio Express 2013 para Windows não criará aplicativos do Windows 8 e da área de trabalho posterior, como os exemplos do SDK do DirectX. Para instalar um dos SKUs Premium do Visual Studio, vá para: [downloads do Visual Studio](https://www.microsoft.com/visualstudio/11/downloads) e siga as instruções.

3.  Use o navegador de exemplo SDK do DirectX para instalar os arquivos de projeto para o exemplo desejado. Abra o arquivo de solução compatível com o Microsoft Visual Studio 2010 do exemplo (sufixos com **\_ 2010**).

4.  Se estiver abrindo o exemplo em um sistema que tenha apenas Microsoft Visual Studio 2012 ou Microsoft Visual Studio 2013 instalado, você receberá a seguinte mensagem: "esta solução contém um ou mais projetos que usam uma versão anterior do compilador e das bibliotecas do VC + +. Cada projeto pode ser atualizado para usar o compilador e as bibliotecas do VC + + (V110). " Escolha a opção **Atualizar** nessa caixa de diálogo para atualizar antes de abrir o projeto.

    Caso contrário, você pode atualizar para o compilador do Visual Studio 2012 ou Visual Studio 2013 C++ 11 e as bibliotecas depois que elas tiverem sido carregadas clicando com o botão direito do mouse na solução e escolhendo **Atualizar projetos do vc + +**.

5.  D3DX não é considerado a API canônica para usar o Direct3D no Windows 8 e versões posteriores e, portanto, não está incluído com o SDK do Windows correspondente. Investigue as soluções alternativas para trabalhar com a API do Direct3D. Para projetos herdados, como os exemplos do SDK do DirectX do Windows 7 (e anteriores), as etapas a seguir são necessárias para criar aplicativos com D3DX usando o SDK do DirectX:

    1.  Modifique os diretórios do **vc + +** do projeto da seguinte maneira para usar a ordem correta para cabeçalhos e bibliotecas do SDK.

        <dl> i. Abra as **Propriedades** do projeto e selecione a página **diretórios do vc + +** .  
        ii. Selecione **todas as configurações e todas as plataformas**.  
        III. Defina esses diretórios da seguinte maneira:

        -   Diretórios executáveis: **<inherit from parent or project defaults>** (na lista suspensa do lado direito)
        -   Diretórios de inclusão: **$ (IncludePath); $ (DXSDK \_ dir) incluem**
        -   Incluir diretórios de biblioteca: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x86**

          
        iv. Clique em **Aplicar**.  
        V. Escolha a **plataforma x64**.  
        VI. Defina o **diretório de biblioteca** da seguinte maneira:

        -   Diretórios de biblioteca: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x64**

          
        </dl>

    2.  Sempre que "d3dx9. h", "d3dx10. h" ou "d3dx11. h" estiverem incluídos em seu projeto, lembre-se de incluir explicitamente "d3d9. h", "d3d10. h" e "dxgi. h", ou "D3D11. h" e "dxgi. h" primeiro para garantir que você está selecionando a versão mais recente. Você pode desabilitar o **C4005 de aviso** , se necessário; no entanto, esse aviso indica que você está usando a versão mais antiga desses cabeçalhos.
    3.  Remova todas as referências a DXGIType. h em seu projeto. Esse cabeçalho não existe no SDK do Windows e a versão do SDK do DirectX está em conflito com o novo Winerror. h.
    4.  Todas as DLLs do D3DX são instaladas em seu computador de desenvolvimento pela instalação do SDK do DirectX. Certifique-se de que as dependências de D3DX necessárias sejam redistribuídas com qualquer amostra ou com seu aplicativo se ele for movido para outro computador.
    5.  Lembre-se de que as tecnologias de substituição para os usos atuais do D3DX11 incluem [DirectXTex](https://github.com/Microsoft/DirectXTex), [DirectXTK](https://github.com/Microsoft/DirectXTK), [DirectXMesh](https://github.com/Microsoft/DirectXMesh)e [UVAtlas](https://github.com/Microsoft/UVAtlas). D3DXMath é substituído por [DirectXMath](./dxmath/directxmath-portal.md).

6.  Verifique se você está usando a nova versão do compilador do sombreador HLSL observando as seguintes condições:

    1.  Alterar o diretório executável de acordo com a etapa 5 fará com que as compilações do projeto usem o FXC da instalação do SDK do Windows. Lembre-se de que os arquivos HLSL agora são oficialmente reconhecidos pelo Visual Studio. Você pode adicioná-los como arquivos de projeto e definir opções de compilador por meio do sistema de projeto.

    2.  Invocar a compilação de tempo de execução por meio da DLL herdada D3DX usará a versão incorreta do compilador HLSL. Substitua todas as referências a \* APIs D3DXCompile, D3DX10Compile \* e D3DX11Compile \* em seu código pela função D3DCompile em D3DCOMPILER \_46.DLL ou D3DCOMPILER \_47.DLL.

    3.  Qualquer projeto que usa a compilação de sombreador de tempo de execução deve ter D3DCOMPILER \_xx.DLL copiado para o caminho do executável local para o projeto. Essa DLL está disponível neste subdiretório da instalação do SDK do Windows em **% ProgramFiles (x86)% \\ Windows kits \\ 8,0 \\ Redist \\ D3D \\ <arch>** ou **% ProgramFiles (x86)% \\ kits do Windows \\ 8,1 \\ Redist \\ D3D \\ <arch>** , em que **<arch>** é **x86** e **x64**.

        O \_47.DLL D3DCOMPILER46.DLL ou D3DCOMPILER \_ da SDK do Windows não é um componente do sistema e não deve ser copiado para o diretório do sistema do Windows. Você pode redistribuir essa DLL para outros computadores com seu aplicativo como uma DLL lado a lado.

7.  Qualquer projeto que use a API XInput e destinado a ser executado no Windows 7 ou em versões anteriores do Windows precisará usar a versão herdada (9.1.0) ou precisará incluir explicitamente os cabeçalhos e as bibliotecas desse componente do SDK do DirectX. O cabeçalho XInput e XINPUT. A LIB incluída no SDK do Windows tem como alvo apenas a versão (1,4) que é fornecida como parte do Windows 8 e posterior. O mesmo cabeçalho pode ser usado com XINPUT9 \_ 1 \_ 0. lib para usar a versão herdada, que está incluída em versões mais antigas do Windows. A versão herdada do XInput não detecta recursos completos ou dá suporte ao áudio integrado ao controlador, portanto, se o suporte para esses recursos for necessário, você deverá usar a versão do SDK do DirectX (1,3).

    Para usar a API XInput de nível inferior completa, você deve ter `#include` os cabeçalhos XInput específicos do SDK do DirectX diretamente:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... e em suas opções de vinculador para dependências adicionais, vincule diretamente à biblioteca XInput do SDK do DirectX:

    **% DXSDK \_ dir% inclui \\ <arch> \\ XInput. lib**

    O \_ binário XINPUT13.DLL é instalado nos diretórios de sistema do Windows pela instalação do SDK do DirectX em seu computador de desenvolvimento. Você precisará redistribuir esse binário com seu aplicativo usando a instalação do DirectX do SDK do DirectX.

8.  Qualquer projeto que usa a API XAudio2 e destinado a ser executado no Windows 7 ou em versões anteriores do Windows precisa usar a versão mais antiga (9.1.0) ou incluir explicitamente os cabeçalhos e as bibliotecas desse componente do SDK do DirectX. Os cabeçalhos e as bibliotecas do XAudio2 que estão incluídos com o SDK do Windows visam apenas a versão (2,8) incluída como parte do Windows 8.

    Por exemplo, com XAudio2, você deve ter `#include` os cabeçalhos XAudio2 específicos do SDK do DirectX diretamente:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... e em suas opções de vinculador para dependências adicionais, vincule diretamente à biblioteca XAudio2 do SDK do DirectX:

    **% DXSDK \_ dir% inclui \\ <arch> \\ XAudio2. lib**

    O \_ binário XAUDIO27.DLL é instalado nos diretórios de sistema do Windows pela instalação do SDK do DirectX em seu computador de desenvolvimento. Você precisa redistribuir essas bibliotecas com seu aplicativo usando a instalação do DirectX do SDK do DirectX.

9.  Se você usou o SDK do DirectX com versões anteriores do Visual Studio, a atualização do Visual Studio 2010 pode ter migrado o caminho do SDK do DirectX para as configurações padrão do projeto. É recomendável que você remova essas configurações para evitar erros futuros de compilação. No diretório **\\ \\ local \\ Microsoft \\ MSBuild \\ v 4.0% USERPROFILE% AppData** , modifique os arquivos **Microsoft. cpp. Win32. User** e **Microsoft. cpp. x64. User** para remover todas as referências a \_ caminhos de dir DXSDK. Como alternativa, você pode remover o <PropertyGroup> nó inteiro que contém as entradas de caminho, como <ExecutablePath> e <IncludePath> para reverter para padrões padrão. Se você não vir referências a DXSDK \_ dir nesses arquivos, nenhuma alteração será necessária.

10. Se o aplicativo resultante oferecer suporte ao Windows Vista com Service Pack 2 (SP2), bem como ao Windows 7 e Windows 8 e posterior, defina a definição de pré-processador chamada **\_ Win32 \_ WinNT** para 0x600. Se ele der suporte apenas ao Windows 7 e Windows 8 e posterior, defina-o como 0x601.

    Por exemplo:

    1.  Abra **as propriedades** do projeto e selecione pré-processador de **C/C++**  >  .
    2.  Selecione **todas as configurações** e **todas as plataformas**.
    3.  Vá para a seção **definições de pré-processador** e defina \_ Win32 \_ WinNT = 0x600.
    4.  Clique em **Aplicar**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Jogos para Windows e SDK do DirectX**
</dt> <dt>

[Onde está o SDK do DirectX (edição 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDKs do DirectX de certa idade](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Viver sem D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
