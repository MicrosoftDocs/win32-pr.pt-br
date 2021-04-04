---
title: Implantação do Direct3D 11 para desenvolvedores de jogos
description: Este artigo descreve como implantar os componentes do Direct3D 11 em um sistema, se necessário.
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162371"
---
# <a name="direct3d-11-deployment-for-game-developers"></a>Implantação do Direct3D 11 para desenvolvedores de jogos

Este artigo descreve como implantar os componentes do Direct3D 11 em um sistema, se necessário.

-   [Visão geral](#overview)
-   [Direct3D 11,3](#direct3d-113)
-   [Direct3D 11,2](#direct3d-112)
-   [Direct3D 11,1](#direct3d-111)
-   [D3D11InstallHelper.dll](#d3d11installhelperdll)
-   [D3D11Install.exe](#d3d11installexe)
-   [Integrando em programas de instalação](#integrating-into-installation-programs)
    -   [Integrando no InstallShield](#integrating-into-installshield)
    -   [Integrando-se a um pacote MSI](#integrating-into-an-msi-package)
-   [Dicas de depuração](#debugging-tips)
-   [Configurações Corporativas](#corporate-settings)
-   [Artigos relacionados](#related-articles)

## <a name="overview"></a>Visão geral

A API do Direct3D 11 estende a API do Direct3D 10,1 existente com suporte para processamento multithread e criação de recursos, sombreador de computação, mosaico de hardware, compactação de textura BC6H/BC7 e modelo de sombreador HLSL 5,0 com vínculo de sombreador dinâmico. Além do componente do Direct3D 11, vários componentes gráficos adicionais estão incluídos no tempo de execução do DirectX 11: Direct3D 11, DXGI 1,1, níveis de recursos do 10level9, dispositivo de renderização de software WARP10, Direct2D, DirectWrite e um Direct3D 10,1 atualizado com suporte para 10level9 e WARP10. Para obter informações sobre esses e outros componentes de gráficos do Windows, consulte [APIs de gráficos no Windows](graphics-apis-in-windows-vista.md).

Todos esses novos componentes gráficos são incorporados aos sistemas operacionais Windows 7 e Windows Server 2008 R2. A API do Direct3D 11 e os componentes relacionados também podem ser instalados no Windows Vista usando uma atualização do sistema do Windows Update; consulte o artigo da base de dados de conhecimento [KB 971644](https://support.microsoft.com/kb/971644). Esta atualização requer o Windows Vista e o Service Pack 2. Os usuários finais com atualizações automáticas habilitadas, portanto, provavelmente já têm os componentes do Direct3D 11 instalados, assim como todos os usuários do Windows 7.

O exemplo de D3D11InstallHelper foi projetado para simplificar a detecção da API do Direct3D 11, instalar automaticamente a atualização do sistema, se aplicável ao computador de um usuário final, e fornecer as mensagens apropriadas ao usuário final sobre o procedimento manual se um Service Pack mais recente for necessário.

> [!Note]  
> O compilador HLSL (D3DCompile \* . dll) e a biblioteca de utilitários D3DX para Direct3D 11 (D3DX11 \* . dll) não são criados em nenhuma versão do sistema operacional Windows, mas podem ser implantados como parte do instalador de um aplicativo usando a tecnologia de DirectSetup existente; para obter mais informações sobre como usar o DirectSetup, consulte [instalação do DirectX para desenvolvedores de jogos](/windows/desktop/DxTechArts/directx-setup-for-game-developers). "Effects 11" está disponível como uma biblioteca de suporte de fonte compartilhada em [efeitos para atualização do Direct3D 11](https://github.com/Microsoft/FX11)e você pode incluí-lo diretamente em um aplicativo (muito parecido com a biblioteca do utilitário DXUT). Portanto, ele não tem nenhum requisito de redistribuição de tempo de execução adicional.

## <a name="direct3d-113"></a>Direct3D 11,3

O Windows 10 é fornecido com a API do Direct3D 11,3 interna. Consulte [recursos do direct3d 11,3](/windows/desktop/direct3d11/direct3d-11-3-features) para obter uma lista dos novos recursos na API do Direct3D 11,3.

## <a name="direct3d-112"></a>Direct3D 11,2

O Windows 8.1 e o Windows Server 2012 R2 são fornecidos com a API do Direct3D 11,2 interna. Consulte [recursos do direct3d 11,2](/windows/desktop/direct3d11/direct3d-11-2-features) para obter uma lista dos novos recursos na API do Direct3D 11,2.

## <a name="direct3d-111"></a>Direct3D 11,1

O Windows 8 e o Windows Server 2012 são fornecidos com a [API do Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) interna. O suporte parcial para a API do Direct3D 11,1 está disponível no Windows 7 ou no Windows Server 2008 R2 com a [atualização da plataforma para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obter mais informações sobre a atualização de plataforma para o Windows 7, consulte [atualização de plataforma para Windows 7](platform-update-for-windows-7.md).

## <a name="d3d11installhelperdll"></a>D3D11InstallHelper.dll

D3D11InstallHelper.dll hospeda a funcionalidade básica para detectar componentes do Direct3D 11 e executar a atualização do sistema por meio do serviço de Windows Update, se aplicável. A DLL não exibe mensagens ou caixas de diálogo diretamente.

A DLL consiste nos seguintes pontos de entrada:

<dl> <dt>

<span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status
</dt> <dd>

Essa função executa as verificações necessárias e retorna o status do Direct3D 11 neste computador. Essa função não requer direitos de administrador.

-   Um status de \_ status D3D11IH \_ instalado indica que o Direct3D 11 já está instalado no computador e está pronto para uso.
-   D3D11IH \_ status \_ sem \_ suporte indica que esta versão do Windows não dá suporte ao Direct3D 11 ou a tecnologias relacionadas.
-   Um status de status de D3D11IH \_ \_ precisa do \_ SP mais recente \_ indica que o Windows Vista Service Pack mais recente deve ser instalado pelo usuário.
-   Por fim, um status de \_ D3D11IH \_ requer \_ atualização indica que o sistema não tem o Direct3D 11 instalado, mas que a atualização do sistema se aplica a esta versão do Windows.

</dd> <dt>

<span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11
</dt> <dd>

Essa função usa a API Windows Update para executar a atualização do sistema para instalar o Direct3D 11 neste sistema, se aplicável. Observe que essa função requer conectividade de rede para Windows Update para obter sucesso, bem como direitos administrativos. Ele usa uma função de retorno de chamada de progresso opcional e um ponteiro de contexto de usuário e retorna um código de resultado final quando concluído.

-   O resultado de êxito do resultado de D3D11IH \_ \_ indica que a atualização do sistema foi aplicada e está pronta para uso, enquanto \_ \_ \_ a reinicialização de resultado do D3D11IH de resultados indica que a atualização do sistema exige que o computador seja reiniciado antes de ser concluído. Observe que essa função não agenda uma reinicialização do sistema.
-   D3D11IH \_ resultado \_ sem \_ suporte indica que a atualização do sistema não se aplica a esta versão do Windows. Esse resultado não deve ocorrer se essa função for chamada somente depois de obter um \_ status de D3D11IH \_ requer \_ status de atualização de CheckDirect3D11Status.
-   Um resultado da atualização do resultado do D3D11IH \_ \_ \_ não \_ encontrado indica que o pacote de atualização do sistema não foi encontrado nos servidores de Windows Update.
-   Se o download ou a instalação do Windows Update falhar, o \_ download da atualização do resultado D3D11IH \_ \_ \_ falha ou \_ \_ a instalação da atualização do resultado D3D11IH \_ \_ será retornada como resultado.
-   Se um erro de conectividade de rede for retornado da API do Windows Update, o \_ resultado do erro do serviço Wu do D3D11IH Result \_ \_ \_ será retornado, indicando que o problema pode ser intermitente ou relacionado à configuração de rede ou configurações de firewall. Tentar a função de atualização novamente pode ter sucesso.

</dd> </dl>

Para obter mais informações sobre a API Windows Update, consulte [Windows Update API do agente](/windows/desktop/Wua_Sdk/portal-client).

## <a name="d3d11installexe"></a>D3D11Install.exe

> [!Note]  
> D3D11Install.exe requer D3D11InstallHelper.dll para ser executado.

D3D11Install.exe é uma ferramenta para usar o D3D11InstallHelper.dll como um instalador autônomo completo com a interface do usuário e mensagens de usuários finais, além de atuar como um exemplo para o uso adequado da DLL. O processo será encerrado com um 0 se o Direct3D 11 já estiver instalado, se a atualização do sistema for aplicada com êxito sem a necessidade de uma reinicialização do sistema, se uma instalação do Service Pack for necessária ou se o Direct3D 11 não tiver suporte neste computador. Um 1 será retornado se a atualização do sistema for aplicada com êxito e exigir que uma reinicialização do sistema seja concluída. Um 2 é retornado para outras condições de erro. Observe que esse arquivo executável exige direitos de administrador para ser executado e tem um manifesto que solicita elevação quando executado no Windows Vista ou no Windows 7 com o UAC habilitado. D3D11Install.exe pode ser usado como uma ferramenta autônoma para implantar a atualização do Direct3D 11 ou pode ser usado diretamente por instaladores.

Ele dá suporte às seguintes opções de linha de comando:

<dl> <dt>

<span id="_quiet__"></span><span id="_QUIET__"></span>/Quiet 
</dt> <dd>

Exibe nenhuma mensagem, prompts, caixas de diálogo de progresso ou mensagens de erro.

</dd> <dt>

<span id="_passive__"></span><span id="_PASSIVE__"></span>/Passive 
</dt> <dd>

Não exibe mensagens, prompts ou mensagens de erro, mas mostrará a caixa de diálogo de progresso.

</dd> <dt>

<span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal 
</dt> <dd>

Mostra apenas os prompts mínimos.

</dd> <dt>

<span id="_y__"></span><span id="_Y__"></span>/y 
</dt> <dd>

Suprime a solicitação para confirmar a instalação da atualização, se necessário e aplicável, para uma instalação padrão e mínima.

</dd> <dt>

<span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/LangID decimal 
</dt> <dd>

Força o código do identificador de idioma a ser usado ao exibir mensagens do usuário final e recursos da caixa de diálogo. O valor padrão é 1024, que usa a configuração de idioma padrão do sistema.

</dd> <dt>

<span id="_wu__"></span><span id="_WU__"></span>/wu 
</dt> <dd>

Força o uso de Windows Update em vez do padrão do sistema, que pode ser Windows Server Update Services (WSUS) em execução em um servidor gerenciado ou alguma outra configuração não padrão.

</dd> </dl>

## <a name="integrating-into-installation-programs"></a>Integrando em programas de instalação

Para estar em conformidade com o suporte à instalação fácil, [requisito técnico 3,1 para jogos para Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006), é necessário tomar cuidado para que todos os prompts do usuário final sejam apresentados no início do processo de instalação e verifique se não há vários prompts de elevação relacionados ao UAC. Há três opções básicas para atingir esse objetivo:

1.  O método mais básico é executar o D3D11Install.exe com a opção de linha de comando **/Minimal**. Isso deve ser feito no início do instalador Q&A, e a instalação deve usar o valor de retorno de 1 para indicar que uma reinicialização deve ser agendada no final da instalação. A execução do programa requer direitos administrativos.
2.  Use D3D11InstallHelper.dll diretamente para detectar a necessidade da atualização, fornecendo qualquer mensagem do usuário final necessária para o status D3D11IH de \_ status \_ necessário \_ SP mais recente \_ , em que a resolução requer operações de usuário manuais. O status do resultado do \_ status D3D11IH \_ não \_ suportado pode ser usado para controlar a instalação de ativos relacionados ao Direct3D 11, ou como uma condição de erro para o Direct3D 11 – somente aplicativos, mas, caso contrário, não é necessariamente uma mensagem útil do usuário final. Para o status D3D11IH de status \_ \_ requer \_ atualização, o instalador pode usar diretamente o ponto de entrada de dll DoUpdateForDirect3D11 para executar a atualização e lidar com as várias mensagens resultantes do usuário final. Exemplos de mensagens padrão podem ser encontrados examinando a caixa de diálogo D3D11Install.exe e os recursos de tabela de cadeia de caracteres. O ponto de entrada de atualização requer direitos de administrador.
3.  Uma abordagem híbrida é verificar o status com D3D11InstallHelper.dll e, no caso do status do código D3D11IH \_ necessário o \_ \_ status mais recente do \_ SP ou do D3D11IH \_ \_ requer \_ Update, D3D11Install.exe pode ser executada com as opções **/Minimal** e **/y** para exibir a caixa de diálogo ou para executar a atualização, conforme necessário. Essas etapas devem ser executadas no início do processo de instalação, normalmente logo após o Q&A e a execução do executável requer direitos administrativos.

### <a name="integrating-into-installshield"></a>Integrando no InstallShield

A manipulação da implantação do Direct3D 11 do InstallScript do InstallShield é feita facilmente usando o exemplo D3D11InstallHelper. As etapas necessárias para integrar com o InstallShield usando o InstallScript são as seguintes (usando o método 3, descrito na seção anterior):

1.  Abra um projeto do InstallScript no editor do InstallShield.
2.  Adicione D3D11InstallHelper.dll e D3D11Install.exe ao projeto em **arquivos de suporte**.

    **Para adicionar os arquivos ao projeto do InstallShield**

    1.  Na guia **Designer de instalação** , clique em **arquivos de suporte/murals** em **comportamento e lógica** no painel de navegação à esquerda.
    2.  Clique em **idioma independente**, clique com o botão direito do mouse na janela **arquivos** e selecione **inserir arquivos**. Navegue até adicionar D3D11InstallHelper.dll e D3D11Install.exe. O local padrão para esses arquivos é: SDK raiz \\ amostras \\ C++ \\ misc \\ bin \\ x86

3.  No Gerenciador de InstallScript, clique no arquivo InstallScript (geralmente setup. RUL) que chamará a DLL ou o executável, localizado em **comportamento e lógica** no painel de navegação à esquerda.
4.  Cole o seguinte InstallScript no arquivo próximo à parte superior:

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  Cole o seguinte InstallScript no arquivo na função **OnFirstUIBefore** , logo antes do retorno 0:

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a>Integrando-se a um pacote MSI

Veja a seguir uma descrição de alto nível das etapas necessárias para integrar a implantação do Direct3D 11 usando as ações personalizadas do MSI (usando o método 3, descrito anteriormente neste tópico):

1.  Adicione uma propriedade à tabela de propriedades do MSI chamada **RelativePathToD3D11IH** que contém o caminho relativo para D3D11Install.exe e D3D11InstallHelper.dll durante a instalação (normalmente, isso ocorre na imagem de mídia). Isso também define um status de D3D11IH \_ da propriedade MSI como o status retornado por CheckDirect3D11Status (uma propriedade de cadeia de caracteres igual ao símbolo de enumeração ou "Error").
2.  Após a ação CostFinalize, chame a função D3D11InstallHelper.dll **SetD3D11InstallMSIProperties** como uma ação personalizada imediata para definir as propriedades apropriadas do MSI para as outras ações personalizadas.
3.  Na instalação, dispare uma ação personalizada adiada após a ação InstallFiles que chama a função de D3D11InstallHelper.dll **DoD3D11InstallUsingMSI**. A ação personalizada deve definir o sinalizador msidbCustomActionTypeNoImpersonate para ser executado em um contexto elevado.
4.  Após a ação InstallFinalize, chame a função D3D11InstallHelper.dll **FinishD3D11InstallUsingMSI** como uma ação personalizada imediata para manipular o código de resultado da solicitação de reinicialização com êxito, se necessário.

Esse procedimento é descrito em detalhes nas instruções a seguir, que descrevem um processo que pode ser feito usando um editor de MSI, como o [Editor Orca](/windows/desktop/Msi/orca-exe). Alguns editores MSI têm assistentes que simplificam algumas dessas etapas de configuração.

**Para configurar um pacote MSI para integração com o D3D11InstallHelper.dll**

1.  Abra o pacote MSI em orca.
2.  Adicione a linha mostrada na tabela a seguir à tabela binária no pacote MSI.

    | Nome    | Dados                                         |
    |---------|----------------------------------------------|
    | D3D11IH | Caminho do arquivo para a DLL \\D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > Esse arquivo será inserido no pacote MSI, portanto, você deve fazer essa etapa toda vez que recompilar D3D11InstallHelper.dll.

     

3.  Adicione as linhas mostradas na tabela a seguir à tabela CustomAction no pacote MSI. 

    | Ação              | Tipo                                                                                                                                                                   | Fonte  | Destino                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | Direct3D11SetProps  | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | SetD3D11InstallMSIProperties |
    | Direct3D11DoInstall | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137 | D3D11IH | DoD3D11InstallUsingMSI       |
    | Direct3D11Finish    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                        | D3D11IH | FinishD3D11InstallUsingMSI   |

    

     

4.  Adicione os valores mostrados para ação, condição e sequência na tabela a seguir à tabela InstallExecuteSequence no pacote MSI. 

    | Ação              | Condição     | Sequência | Observações                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Direct3D11SetProps  |               | 1016     | O número de sequência coloca a ação logo após CostFinalize.                                                                                                 |
    | Direct3D11DoInstall | NÃO instalado | 4004     | Essa ação personalizada só ocorrerá durante uma nova instalação para todos os usuários. O número de sequência coloca a ação após InstallFiles e após as reversões. |
    | Direct3D11Finish    |               | 6615     | O número de sequência coloca a ação logo após InstallFinalize.                                                                                              |

    

     

5.  Adicione a linha mostrada na tabela a seguir à tabela de **Propriedades** no pacote MSI. 

    | Propriedade              | Valor                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | RelativePathToD3D11IH | caminho de arquivo relativo que contém D3D11Install.exe e D3D11InstallHelper.dll |

    

     

    > [!Note]  
    > O local especificado pelo caminho é relativo ao local especificado pelo caminho de instalação — por exemplo, "Redist \\ ".

     

6.  Salve o pacote MSI. Para obter informações mais detalhadas sobre pacotes e Windows Installer do MSI, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Dicas de depuração

Tanto D3D11InstallHelper.dll quanto D3D11Install.exe podem ser compilados com a configuração de depuração no Visual Studio, e essas versões imprimirão mensagens para o mecanismo de saída de depuração padrão do Windows.

## <a name="corporate-settings"></a>Configurações Corporativas

O exemplo D3D11InstallHelper foi projetado para implantação padrão por meio de Windows Update, que é o cenário mais comum para a instalação de um jogo por consumidores. No entanto, muitos desenvolvedores de jogos, trabalhando para editores e estúdios de desenvolvimento, fazem isso em configurações corporativas que têm um servidor gerenciado localmente fornecendo atualizações de software usando a tecnologia Windows Server Update Services (WSUS). Nesse tipo de ambiente, o administrador de ti local tem controle de aprovação sobre quais atualizações são disponibilizadas para computadores na rede corporativa, e a versão de consumidor padrão da atualização KB 971644 não está disponível.

Há três soluções básicas para implantar o DirectX 11 em configurações corporativas/corporativas:

-   Em algumas configurações, é possível verificar diretamente Windows Update em vez de usar o servidor WSUS gerenciado localmente. Por esse motivo, o D3D11InstallHelper dá suporte à opção de linha de comando **/Wu** . No entanto, nem todas as redes corporativas permitem conexões com os servidores públicos da Microsoft.
-   O administrador de ti local pode aprovar o KB 971512, uma atualização com suporte da empresa implantada do WSUS, que inclui a API do Direct3D 11. Essa é a única opção para um usuário padrão obter a atualização do Direct3D 11 em um ambiente totalmente bloqueado.
-   Como alternativa, o [KB 971512](https://support.microsoft.com/kb/971512/) pode ser instalado manualmente.

É muito raro que o computador de um jogador possa obter apenas atualizações de um servidor WSUS gerenciado localmente, e é apenas desenvolvedores em grandes organizações que provavelmente estejam em ambientes.

## <a name="related-articles"></a>Artigos relacionados

[Firewall do Windows para Desenvolvedores de Jogos](/windows/desktop/DxTechArts/games-and-firewalls)

[Explorador de jogos do Windows para desenvolvedores de jogos](/windows/desktop/DxTechArts/windows-game-explorer-integration)