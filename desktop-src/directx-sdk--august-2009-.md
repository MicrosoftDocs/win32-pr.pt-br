---
description: a partir do Windows 8, o SDK do DirectX é incluído como parte do SDK do Windows.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Onde está o SDK do DirectX?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46559e839abea9d6e0c89ab7e5940e46b2d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886458"
---
# <a name="where-is-the-directx-sdk"></a>Onde está o SDK do DirectX?

a partir do Windows 8, o SDK do DirectX é incluído como parte do SDK do Windows.

Criamos originalmente o SDK do DirectX como uma plataforma de alto desempenho para desenvolvimento de jogos sobre o Windows. À medida que as tecnologias do DirectX amadureceram, elas se tornaram relevantes para uma gama mais ampla de aplicativos. Hoje, a disponibilidade do hardware de Direct3D em computadores impulsiona os aplicativos de área de trabalho tradicionais para usar aceleração de hardware de gráficos. Em paralelo, as tecnologias do DirectX são mais integradas ao Windows. Agora, o DirectX é uma parte fundamental do Windows.

como o SDK do Windows é o principal SDK do desenvolvedor do Windows, o DirectX agora está incluído nele. agora você pode usar o SDK do Windows para criar jogos incríveis para Windows. para baixar o sdk do Windows 8. x ou o sdk do Windows 10, consulte [SDK do Windows e arquivo de emulador](https://developer.microsoft.com/windows/downloads/sdk-archive).

as tecnologias e ferramentas a seguir, anteriormente parte do SDK do DirectX, agora fazem parte do SDK do Windows.


| Tecnologia ou ferramenta | Description | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Componentes gráficos<br /> | os cabeçalhos e bibliotecas para <a href="/windows/desktop/direct3d">Direct3D</a> e outras APIs de gráficos de Windows, como <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, estão disponíveis no SDK do Windows. <br /><blockquote>[!Note]<br />as bibliotecas do utilitário preterido D3DX9/D3DX10/D3DX11 estão disponíveis por meio de <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, mas também há uma série de <a href="https://walbourn.github.io/living-without-d3dx/">alternativas de código aberto</a>. a biblioteca do utilitário D3DCSX DirectCompute e a DLL redistribuível estão disponíveis no SDK do Windows. D3DX12 está disponível em <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilador HLSL (FXC.EXE)<br /> | o compilador <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> é uma ferramenta no subdiretório de arquitetura apropriado na pasta bin do SDK do Windows.<br /><blockquote>[!Note]<br />a API D3DCompiler e a DLL redistribuível estão disponíveis no SDK do Windows.</blockquote><br /><br />para o desenvolvimento do DirectX 12, use o DXCompiler no SDK do Windows e hospedado em [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX para Windows<br /> | uma substituição para a ferramenta PIX for Windows agora é um recurso no Microsoft Visual Studio, chamado depurador de gráficos Visual Studio. esse recurso melhorou muito a usabilidade, o suporte para Windows 8 e o Direct3D 11,1 e a integração com recursos tradicionais de Microsoft Visual Studio, como pilhas de chamadas e janelas de depuração para depuração <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Para obter mais informações sobre esse novo recurso, consulte <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">depuração de elementos gráficos do DirectX</a>.<br /><br />Para o desenvolvimento do DirectX 12, consulte a última geração de <a href="https://devblogs.microsoft.com/pix/">PIX no Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> para Windows<br /> | a API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> agora é um componente do sistema em Windows 8. x e Windows 10. os cabeçalhos e as bibliotecas para XAudio2 estão disponíveis no SDK do Windows. para obter suporte a Windows 7, consulte <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> para Windows<br /> | a API do <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 agora é um componente do sistema em Windows 8. x e Windows 10. os cabeçalhos e as bibliotecas para XInput estão disponíveis no SDK do Windows.<br /><blockquote>[!Note]<br />o XInput 9.1.0 herdado também está disponível como parte do Windows 7 ou posterior.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br /> | A versão mais recente do XNAMATH, que é atualizada para novos conjuntos de instruções, bem como ARM/ARM64, agora é <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. os cabeçalhos para DirectXMath estão disponíveis na SDK do Windows e em <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Painel de controle do DirectX e visualizador de recursos do DirectX<br /> | os utilitários do painel de controle do directx e do visualizador de recursos do directx estão incluídos no subdiretório de arquitetura apropriado na pasta bin do SDK do Windows. O Visualizador de recursos do DirectX também está disponível em <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACTSET<br /> | A ferramenta de multiplataforma de áudio Xbox (transação) não tem mais suporte para uso em Windows.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de jogos</a> e GDFMAKER<br /> | A API do <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de jogos</a> apresenta jogos para os usuários de Windows. a API do explorador de jogos tem suporte apenas no Windows Vista e Windows 7. Use a ferramenta criador de arquivos de definição de jogos (GDFMAKER.EXE) para declarar classificações de jogos para aplicativos da loja Windows. <br /> a ferramenta criador de arquivos de definição de jogos (GDFMaker.exe) está incluída no subdiretório x86 sob a pasta bin na SDK do Windows e dá suporte a aplicativos de Windows de armazenamento e aplicativos de área de trabalho do Win32.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Exemplos<br /> | você pode encontrar aplicativos de exemplo que realçam as tecnologias directx 12 em Windows no repositório de <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">exemplos do directx</a> . A maioria dos exemplos de versões mais antigas do Direct3D também está disponível online. Para obter mais informações sobre esses exemplos, consulte <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catálogo de exemplos do SDK do DirectX</a>.<br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 gerenciado<br /> | Os assemblies do .NET DirectX são preteridos e não são recomendados para uso por novos aplicativos. Há várias alternativas disponíveis. Consulte <a href="https://walbourn.github.io/directx-and-net/">DirectX e .net</a>. <br /> | 




 

O SDK do DirectX herdado está disponível para download no [centro de download da Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) , se necessário, mas o uso para novos projetos não é recomendado.

> [!Note]  
> O SDK do DirectX não será instalado se você tiver uma determinada versão do pacote redistribuível do Visual C++ 2010 já instalado. Para obter mais informações sobre o e uma solução para corrigir esse problema, consulte [o erro "S1023" ao instalar o SDK do DirectX (junho de 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Usando projetos SDK do DirectX com Visual Studio

os exemplos do SDK do DirectX de junho de 2010 têm suporte com SKUs Visual Studio premium (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 ou Microsoft Visual Studio Ultimate 2013) no Windows 7 e nas versões Windows 8 e posteriores. devido à transição de cabeçalhos e bibliotecas do DirectX para o SDK do Windows, as alterações nas configurações do projeto são necessárias para criar esses exemplos corretamente com o modo como o SDK do Windows 8 e posterior é empacotado com as SKUs do Visual Studio premium.

Essas etapas também se aplicam aos seus próprios projetos que dependem do SDK do DirectX.

1.  Verifique se a versão de junho de 2010 do SDK do DirectX está instalada no seu computador de desenvolvimento. se você instalar o em um computador que executa o Windows 8 e posterior, será solicitado e necessário habilitar o .net 3,5 como uma instalação de pré-requisito para o SDK do DirectX.

    > [!Note]  
    > O SDK do DirectX não será instalado se você tiver uma determinada versão do pacote redistribuível do Visual C++ 2010 já instalado. Para obter mais informações sobre o e uma solução para corrigir esse problema, consulte [o erro "S1023" ao instalar o SDK do DirectX (junho de 2010)](https://support.microsoft.com/kb/2728613).

     

2.  verifique se você está usando uma das SKUs do Visual Studio premium. Microsoft Visual Studio Express 2012 para Windows 8 ou Microsoft Visual Studio Express 2013 para Windows não criará Windows 8 e aplicativos de área de trabalho posteriores, como os exemplos do SDK do DirectX. para instalar uma das SKUs do Visual Studio premium, vá para: [Visual Studio downloads](https://www.microsoft.com/visualstudio/11/downloads) e siga as instruções.

3.  Use o navegador de exemplo SDK do DirectX para instalar os arquivos de projeto para o exemplo desejado. abra o arquivo de solução compatível com o Microsoft Visual Studio 2010 do exemplo (sufixos com **\_ 2010**).

4.  se estiver abrindo o exemplo em um sistema que tenha apenas Microsoft Visual Studio 2012 ou Microsoft Visual Studio 2013 instalado, você receberá a seguinte mensagem: "esta solução contém um ou mais projetos que usam uma versão anterior do compilador VC++ e bibliotecas. cada projeto pode ser atualizado para usar o compilador de VC++ e bibliotecas (v110). " Escolha a opção **Atualizar** nessa caixa de diálogo para atualizar antes de abrir o projeto.

    caso contrário, você pode atualizar para o compilador Visual Studio 2012 ou Visual Studio 2013 C++ 11 e as bibliotecas depois que elas tiverem sido carregadas clicando com o botão direito do mouse na solução e escolhendo **atualizar projetos de VC++**.

5.  D3DX não é considerado a API canônica para usar o Direct3D no Windows 8 e posterior e, portanto, não está incluído com o SDK do Windows correspondente. Investigue as soluções alternativas para trabalhar com a API do Direct3D. para projetos herdados, como os exemplos do SDK do directx do Windows 7 (e anteriores), as etapas a seguir são necessárias para criar aplicativos com D3DX usando o SDK do directx:

    1.  modifique os diretórios de **VC++** do projeto da seguinte maneira para usar a ordem correta para cabeçalhos e bibliotecas do SDK.

        <dl> i. abra as **propriedades** do projeto e selecione a página **diretórios de VC++** .  
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
    3.  Remova todas as referências a DXGIType.h em seu projeto. Esse título não existe no SDK do Windows, e a versão do SDK do DirectX entra em conflito com o novo winerror.h.
    4.  Todas as DLLs D3DX são instaladas em seu computador de desenvolvimento pela instalação do SDK do DirectX. Certifique-se de que as dependências D3DX necessárias sejam redistribuídas com qualquer exemplo ou com seu aplicativo se ele for movido para outro computador.
    5.  Esteja ciente de que as tecnologias de substituição para usos atuais do D3DX11 incluem [DirectXTex,](https://github.com/Microsoft/DirectXTex) [DirectXTK,](https://github.com/Microsoft/DirectXTK) [DirectXMesh](https://github.com/Microsoft/DirectXMesh)e [UVAtlas.](https://github.com/Microsoft/UVAtlas) D3DXMath é substituído por [DirectXMath.](./dxmath/directxmath-portal.md)

6.  Verifique se você está usando a nova versão do compilador de sombreador HLSL observando as seguintes condições:

    1.  Alterar o diretório executável de acordo com a etapa 5 fará com que os builds de projeto usem o FXC da instalação Windows SDK. Esteja ciente de que os arquivos HLSL agora são oficialmente reconhecidos pelo Visual Studio. Você pode adicioná-los como arquivos de projeto e definir opções do compilador por meio do sistema de projeto.

    2.  Invocar a compilação em tempo de executar por meio da DLL D3DX herdada usará a versão mais antiga incorreta do compilador HLSL. Substitua todas as referências às APIs D3DXCompile \* , D3DX10Compile e D3DX11Compile em seu código pela \* função \* D3DCompile em D3DCOMPILER \_46.DLL ou D3DCOMPILER \_47.DLL.

    3.  Qualquer projeto que usa a compilação do sombreador em tempo de execução deve ter osxx.DLL D3DCOMPILER copiados para o caminho \_ executável local para o projeto. Essa DLL está disponível neste subdjunto da instalação do SDK do Windows em **%ProgramFiles(x86)% \\ Windows Kits \\ 8.0 \\ Redist \\ D3D \\ &lt; ou &gt;** **%ProgramFiles(x86)% \\ Windows Kits \\ 8.1 \\ Redist \\ D3D \\ &lt; &gt; em** que **&lt; arch &gt;** é **x86** **e x64**.

        O47.DLL \_ D3DCOMPILER46.DLL ou D3DCOMPILER do SDK do Windows não é um componente do sistema e não deve ser copiado para o diretório \_ Windows sistema. Você pode redistribuir essa DLL para outros computadores com seu aplicativo como uma DLL lado a lado.

7.  Qualquer projeto que usa a API XInput e se destina a ser executado no Windows 7 ou versões mais antigas do Windows precisa usar a versão herdada (9.1.0) ou precisará incluir explicitamente os headers e bibliotecas para esse componente do SDK do DirectX. O header XInput e XINPUT. LIB que estão incluídos no SDK Windows destino somente a versão (1.4) que é fornecidas como parte Windows 8 e posterior. O mesmo header pode ser usado com XINPUT9 \_ 1 0.LIB para usar a versão herdada, que está incluída em versões mais antigas \_ do Windows. A versão herdada do XInput não detecta recursos completos nem dá suporte a áudio integrado ao controlador, portanto, se o suporte para esses recursos for necessário, você deverá usar a versão do SDK do DirectX (1.3).

    Para usar a API XInput de nível inferior completo, você deve os headers XInput específicos do `#include` SDK do DirectX diretamente:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... e nas opções do linker para Dependências Adicionais, vincule diretamente à biblioteca XInput do SDK do DirectX:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xinput.lib**

    O binário3.DLL XINPUT1 é instalado nos Windows do sistema pela instalação do SDK do DirectX em seu computador \_ de desenvolvimento. Você precisará redistribuir esse binário com seu aplicativo usando a instalação da Instalação do DirectX do SDK do DirectX.

8.  Qualquer projeto que usa a API XAudio2 e se destina a ser executado no Windows 7 ou versões mais antigas do Windows precisa usar a versão mais antiga (9.1.0) ou incluir explicitamente os headers e bibliotecas para esse componente do SDK do DirectX. Os bibliotecas e os headers XAudio2 incluídos no SDK do Windows são destinados apenas à versão (2.8) incluída como parte do Windows 8.

    Por exemplo, com XAudio2, você deve ter os headers XAudio2 específicos do `#include` SDK do DirectX diretamente:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... e, em suas opções de vinculador para Dependências Adicionais, vincule diretamente à biblioteca XAudio2 do SDK do DirectX:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xaudio2.lib**

    O binário7.DLL XAUDIO2 é instalado nos Windows do sistema pela instalação do SDK do DirectX em \_ seu computador de desenvolvimento. Você precisa redistribuir essas bibliotecas com seu aplicativo usando a instalação da Instalação do DirectX do SDK do DirectX.

9.  Se você usou o SDK do DirectX com versões anteriores do Visual Studio, a atualização do Visual Studio 2010 pode ter migrado o caminho do SDK do DirectX para as configurações padrão do projeto. É recomendável remover essas configurações para evitar erros de build futuros. No **diretório %USERPROFILE% \\ AppData \\ Local microsoft MSBuild \\ \\ \\ v4.0,** modifique os arquivos **Microsoft.Cpp.Win32.user** e **Microsoft.Cpp.x64.user** para remover todas as referências aos caminhos DXSDK \_ DIR. Como alternativa, você pode remover todo o nó PropertyGroup que contém as entradas Path, como &lt; &gt; ExecutablePath e &lt; &gt; &lt; IncludePath, para reverter para &gt; os padrões padrão. Se você não vir referências ao DXSDK \_ DIR nesses arquivos, nenhuma alteração será necessária.

10. Se o aplicativo resultante for compatível com Windows Vista com Service Pack 2 (SP2), bem como Windows 7 e Windows 8 e posteriores, de definir a Definição do Pré-processador denominada **\_ WIN32 \_ WINNT** como 0x600. Se ele só dá suporte Windows 7 e Windows 8 e posteriores, de definido como 0x601.

    Por exemplo:

    1.  Abra **Propriedades** para o projeto e selecione **Pré-processador C/C++.**  >  
    2.  Selecione **Todas as Configurações** e **Todas as Plataformas**.
    3.  Vá para a **seção Definições do Pré-processador** e defina \_ WIN32 \_ WINNT=0x600.
    4.  Clique em **Aplicar**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Jogos para Windows e SDK do DirectX**
</dt> <dt>

[Onde está o SDK do DirectX (Edição 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDKs do DirectX de uma determinada idade](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Morando sem D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
