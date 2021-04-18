---
title: Programa de aplicativo da área de trabalho do Windows
description: Você pode obter dados de telemetria e relatórios de análise detalhados que permitem ver como os aplicativos da área de trabalho do Windows estão fazendo por meio do novo programa de aplicativos da área de trabalho do Windows.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 2dc255c9c8696bd57198f50fc2c570f59c4ae603
ms.sourcegitcommit: 0bfbb2324081644171495734f0609335173745ef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2021
ms.locfileid: "105763316"
---
# <a name="windows-desktop-application-program"></a>Programa de aplicativo da área de trabalho do Windows

Você pode obter dados de telemetria e relatórios de análise detalhados que permitem ver como os aplicativos da área de trabalho do Windows estão fazendo por meio do novo programa de aplicativos da área de trabalho do Windows.

Não há nenhum custo para acessar esses dados, tudo o que você precisa fazer é [inscrever-se](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) e aceitar o [contrato do programa de aplicativos da área de trabalho do Windows](https://go.microsoft.com/fwlink/?linkid=853677)e, em seguida, carregar um arquivo assinado usando o mesmo certificado usado para assinar os arquivos executáveis do aplicativo.

## <a name="join-the-windows-desktop-application-program"></a>Participe do programa de aplicativos da área de trabalho do Windows

**Se sua empresa já tiver uma conta do Partner Center**: entre na sua conta do Partner Center (usando o conta Microsoft associado ao proprietário da conta) e navegue até a página **programas** (em **configurações da conta** ou selecionando **tudo** no menu de navegação à esquerda). Em **programa de aplicativos da área de trabalho do Windows**, clique em **introdução** para ingressar no programa sem custo adicional. Se você tiver um locatário do Azure AD associado à sua conta do Partner Center, os usuários que você adicionou poderão acessar o programa de aplicativos da área de trabalho do Windows. Em breve, nós lhe permitimos que você defina um acesso mais granular para esse programa.

> [!Tip]  
> Se sua empresa tiver uma conta do Partner Center, mas você não tiver acesso a ela, peça ao administrador para adicioná-lo [como um usuário](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Observe que apenas o proprietário da conta pode ingressar no programa de aplicativo da área de trabalho do Windows.

 

**Se sua empresa não tiver uma conta do Partner Center**: você poderá [se inscrever no programa de aplicativos da área de trabalho do Windows diretamente](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) sem nenhum custo. Em breve, forneceremos a opção de [associar um locatário do Azure ad à sua conta](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) para que outras pessoas em sua empresa também possam entrar.

## <a name="add-your-desktop-applications"></a>Adicionar seus aplicativos de área de trabalho

Depois de ingressar no programa, você precisará adicionar seus aplicativos da área de trabalho do Windows ao seu painel para que possamos começar a mostrar seus relatórios de análise.

Usamos a assinatura de código para estabelecer a identidade da sua empresa e recuperar a análise para aplicativos que você publica.

Forneceremos um arquivo e solicitaremos que você o assine com os mesmos certificados de assinatura de código não revogados válidos e não expirados que você usa para assinar seus aplicativos de área de trabalho. Depois disso, você carregará esse arquivo assinado em seu painel. Isso nos permite saber que todos os aplicativos da área de trabalho assinados com o mesmo certificado pertencem à sua conta. Não usamos suas informações de certificado para nenhuma outra finalidade.

> [!Important]  
> Você não precisa repetir esse processo se você liberar um novo aplicativo de área de trabalho. Depois de carregar o arquivo assinado, nós identificaremos automaticamente todos os novos aplicativos assinados com o mesmo certificado e recuperaremos automaticamente a análise para esses produtos. Você também não precisa distribuir o arquivo fornecido em seus aplicativos ou enviar qualquer tipo de mapeamento para seus produtos

 

**Para adicionar um ou mais aplicativos de área de trabalho**

1.  No painel, selecione **adicionar aplicativos de área de trabalho**.
2.  Na página seguinte, baixe o arquivo que pode ser assinado selecionando **baixar o arquivo** e salve o arquivo em seu computador.
3.  Assine o arquivo que você acabou de baixar usando o mesmo certificado de assinatura de código que você usa para autenticar seus aplicativos de área de trabalho. Você pode usar SignTool.exe (disponível em Microsoft Visual Studio e como parte do [SDK do Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk)) para assinar esse arquivo. Mais detalhes sobre esse processo estão descritos abaixo.
4.  Carregue o arquivo que você acabou de assinar, arrastando-o para o campo (ou clique para procurar seus arquivos).
5.  Selecione **Enviar** para concluir o processo.

![etapas para adicionar aplicativos de área de trabalho](images/uploadcert.png)

Se você usar mais de um certificado de assinatura de código, poderá repetir as etapas acima para cada um de seus certificados. Você pode baixar, assinar e carregar um arquivo para cada certificado atual que você usa para assinar seus aplicativos. No entanto, você só pode usar um certificado por arquivo baixado.

Depois de concluir essas etapas, identificaremos quais aplicativos da área de trabalho do Windows são assinados com o mesmo certificado que você usou para assinar nosso arquivo. Na maioria dos casos, começaremos a mostrar os relatórios analíticos dentro de 48 horas, embora possa levar um pouco mais tempo.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Usar signtool.exe para assinar o arquivo baixado

A Microsoft fornece uma ferramenta para assinar arquivos, SignTool.exe, com o Visual Studio e no [SDK do Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk). Você pode usar essa ferramenta para executar e verificar o processo de assinatura de código. Mais informações sobre o SignTool.exe estão disponíveis [aqui](/dotnet/framework/tools/signtool-exe).

Aqui estão duas das maneiras mais comuns de usar essa ferramenta para assinar o arquivo que pode ser assinado.

-   Se você tiver acesso ao certificado de assinatura de código como um arquivo de [troca de informações pessoais (pfx)](/windows-hardware/drivers/install/personal-information-exchange---pfx--files) :

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Captura de tela que mostra uma janela de prompt de comando mostrando o comando ' Signtool sinal/f MyCert. pfx/p MyCertPassword/v SignableFile. bin '.](images/signtool2.png)

-   Se o certificado de assinatura de código estiver disponível em seu repositório de certificados local:

    ``` syntax
    Signtool sign /v /s MY /n CertSubjectName SignableFile.bin
    ```

    ![janela do prompt de comando mostrando este comando](images/signtool.png)

Depois de assinar o arquivo, você pode verificar se ele foi assinado com êxito com um certificado válido com o seguinte:

``` syntax
signtool verify /a SignableFile.bin
```

## <a name="viewing-your-analytic-data"></a>Exibindo seus dados analíticos

Depois que os arquivos assinados tiverem sido carregados e identificarmos seus aplicativos de desktop, seu painel mostrará uma visão geral de seus aplicativos, juntamente com as principais métricas.

Nossos dados de telemetria mostrarão informações de integridade, como falhas para cada aplicativo associado ao seu certificado. Seu painel mostrará uma visão geral de seus aplicativos, juntamente com as métricas-chave. Você pode selecionar qualquer aplicativo para exibir seu relatório de [integridade](#health-report), [instalar relatório](#installs-report)e [Bloquear relatório](#application-blocks-report) no painel. Você também pode [recuperar dados analíticos programaticamente usando a API de análise de Microsoft Store](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Se detectarmos que os metadados de um aplicativo foram atualizados para usar um novo nome, começaremos a relatar novos dados com o novo nome. Os dados históricos associados ao nome antigo serão preservados por 30 dias.
> 
> A análise não estará disponível para um aplicativo até que ele tenha sido instalado em pelo menos 100 dispositivos.


### <a name="health-report"></a>Relatório de integridade

O relatório de **integridade** permite que você obtenha dados relacionados ao desempenho e à qualidade do seu aplicativo, incluindo falhas e eventos sem resposta. Onde for aplicável, você pode exibir rastreamentos de pilha e/ou arquivos CAB para depuração adicional.

![relatório de integridade-programa de aplicativos para área de trabalho do Windows](images/health.png)

Você pode filtrar os dados de várias maneiras, permitindo:

-   Exibir um resumo de todos os tipos de falha, classificados por número de ocorrências
-   Faça uma busca detalhada em uma falha específica e baixe os rastreamentos de pilha para depurar o problema mais rapidamente
-   Comparar uma nova versão do seu aplicativo com as versões anteriores
-   Exibir dados de integridade em agregação ou por região, permitindo isolar problemas específicos de uma região
-   Compare o desempenho de seus aplicativos de desktop em versões do Windows ou em uma versão específica, como a versão mais recente do Windows 10
-   Exibir informações de integridade para um arquivo executável específico incluído em seu aplicativo

Selecione **carregar símbolos** na parte superior da tabela **falhas** para carregar um arquivo. zip que contém os arquivos de [símbolo](http:/docs.microsoft.com/windows-hardware/drivers/debugger/symbols-and-symbol-files)do aplicativo. Esses arquivos de símbolos serão indexados e usados para produzir rastreamentos de pilha mais precisos. Os tipos de arquivo de símbolo dentro de. zip devem ser. pdb,. dll ou. exe. Depois de carregar com êxito o arquivo. zip, você verá menos **! Valores desconhecidos** para novas falhas na lista de falhas do aplicativo em aproximadamente 5 dias.

### <a name="installs-report"></a>Relatório de instalações

O relatório de **instalações** permite ver quantos dispositivos um aplicativo foi instalado em um determinado dia e o número médio de dispositivos em que cada versão do aplicativo foi instalada nos últimos 30 dias.

Você pode filtrar os dados de várias maneiras, permitindo:

-   Exibir um resumo de suas instalações, classificadas por popularidade
-   Comparar uma nova versão do seu aplicativo com as versões anteriores
-   Exibir dados de instalação em agregação ou por região
-   Compare o desempenho de seus aplicativos de desktop em versões do Windows ou em uma versão específica, como a versão mais recente do Windows 10 ou versões mais rápidas e lentas do Windows Insider

### <a name="application-blocks-report"></a>Relatório de blocos de aplicativo

O relatório **blocos de aplicativos** permite que você veja informações sobre dispositivos Windows 10 nos quais seu aplicativo está afetando as atualizações do Windows 10. Você pode ver quantos dispositivos são afetados em um determinado dia, juntamente com o número médio de dispositivos nos últimos 30 dias.

Os tipos de blocos de atualização incluídos são os seguintes: 

<table>
<tr><th>Category</th><th>Problema</th><th>Descrição</th><th>Diretrizes fornecidas aos usuários</th></tr>
<tr><td>Potencial SEDIMENT</td><td>Bloqueará a atualização</td><td>O aplicativo não funcionará na nova versão de lançamento do sistema operacional. A ação do usuário é necessária durante a instalação para prosseguir com a atualização.</td><td>Remova o aplicativo antes de atualizar e verifique com o desenvolvedor uma versão compatível do aplicativo.</td></tr>
<tr><td>SEDIMENT temporário</td><td>Pode bloquear a atualização. É necessário testar o aplicativo.</td><td>A Microsoft está investigando problemas de atualização relacionados a este aplicativo. A atualização não será distribuída para os usuários que podem ser afetados.</td><td>Remova o aplicativo antes de atualizar e verifique com o desenvolvedor uma versão compatível do aplicativo.</td></tr>
<tr><td>Notificação de tempo de execução</td><td>Pode não funcionar corretamente na nova versão de lançamento do sistema operacional, mas não bloqueará a atualização</td><td>O aplicativo não impedirá a atualização, mas foram detectados problemas que podem impedi-lo de funcionar corretamente na nova versão de lançamento do sistema operacional.</td><td>Nenhuma ação é necessária para que a atualização Continue, mas certifique-se de testar o aplicativo na nova versão de lançamento do sistema operacional e verifique com o desenvolvedor uma versão compatível, se necessário.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Recuperar dados analíticos usando a API de análise de Microsoft Store

A API de análise de Microsoft Store permite recuperar dados de análise programaticamente para aplicativos que você adicionou à sua conta.

Essa API oferece os seguintes métodos específicos para o programa de aplicativos da área de trabalho do Windows:

-   [Instalada](/windows/uwp/monetize/get-desktop-app-installs)
-   [Ocorrências de falha](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Detalhes da falha](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Rastreamento de pilha](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [Arquivo CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Blocos de atualização](/windows/uwp/monetize/get-desktop-block-data)
-   [Detalhes do bloco de atualização](/windows/uwp/monetize/get-desktop-block-data-details)


Para obter mais informações sobre como usar essa API, consulte [acessar dados analíticos usando os serviços de loja](/windows/uwp/monetize/access-analytics-data-using-windows-store-services).

## <a name="managing-your-desktop-application-metadata"></a>Gerenciando os metadados do aplicativo da área de trabalho

Usamos o nome do arquivo, a versão do arquivo, o nome do produto e os metadados da versão do produto em seus arquivos executáveis para inferir os agrupamentos lógicos de executáveis em aplicativos. Se os arquivos executáveis não tiverem metadados precisos, eles poderão aparecer juntos em um nome de aplicativo **desconhecido** ou o nome do aplicativo usará como padrão o nome do executável individual.

Manter os metadados dos seus aplicativos e arquivos atualizados ajuda a garantir que eles sejam representados corretamente em seu painel. Aqui estão algumas recomendações:

-   Use seu certificado para assinar todos os arquivos executáveis que você deseja ver no relatório de análise, não apenas os executáveis de instalação.
-   Forneça informações consistentes sobre o nome do produto e a versão do produto para todos os arquivos executáveis que pertencem ao mesmo aplicativo (ou seja, *meu aplicativo*). Se alguns dos seus arquivos executáveis forem distribuídos com vários aplicativos, forneça nomes exclusivos (ou seja, *componentes compartilhados*) para que você possa ver análises para esses executáveis separadamente dos aplicativos com os quais foram distribuídos.
-   Sempre que você fizer alterações em seus metadados, poderá ver uma nova entrada para seu aplicativo em seu painel. Se você fizer uma alteração, novos dados de telemetria de entrada refletirão suas alterações, mas seus dados de telemetria antigos ainda aparecerão como um aplicativo **desconhecido** .
-   Ao revisar um arquivo, certifique-se de atualizar a versão do aplicativo e os números de versão do produto.
    > [!Tip]  
    > Use os recursos do [**VERSIONINFO**](/windows/desktop/menurc/versioninfo-resource) para definir o arquivo de **Descrição**, **FileVersion**, **ProductName** e **ProductVersion** para seus arquivos e aplicativos. O exemplo a seguir define um recurso **VERSIONINFO** :
    >
    > ``` syntax
    > #define VER_PRODUCTNAME_STR      "Sample App"
    > #define VER_PRODUCTVERSION       3,10,349,0
    > #define VER_PRODUCTVERSION_STR   "3.10.349.0\0"
    > #define VER_FILEDESCRIPTION_STR  "Sample File"
    > #define VER_FILEVERSION          3,10,349,0
    > #define VER_FILEVERSION_STR      "3.10.349.0\0"
    > #define VER_COMPANYNAME_STR     "XYZ Corp."
    > #define VER_LEGALCOPYRIGHT_STR   "Copyright \251 XYZ Corp." 
    >  
    > VS_VERSION_INFO VERSIONINFO
    > FILEVERSION VER_FILEVERSION
    > PRODUCTVERSION VER_PRODUCTVERSION
    > FILEFLAGSMASK VER_FILEFLAGSMASK
    > FILEFLAGS VER_FILEFLAGS
    > FILEOS VER_FILEOS
    > FILETYPE VER_FILETYPE
    > FILESUBTYPE VER_FILESUBTYPE
    > BEGIN
    >     BLOCK "StringFileInfo"
    >     BEGIN
    >         BLOCK "040904E4"
    >         BEGIN
    >             VALUE "ProductName",      VER_PRODUCTNAME_STR
    >             VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
    >             VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
    >             VALUE "FileVersion",      VER_FILEVERSION_STR
    >             VALUE "CompanyName",      VER_COMPANYNAME_STR
    >             VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
    >         END
    >     END
    >      
    > END 
    > ```

     

## <a name="add-and-manage-account-users"></a>Adicionar e gerenciar usuários da conta

Você pode usar Azure Active Directory para adicionar e gerenciar usuários adicionais na sua conta de programa de aplicativo da área de trabalho do Windows. Você pode adicionar usuários individuais, grupos de usuários ou aplicativos do Azure AD, fornecendo a cada um uma função predefinida (gerente ou desenvolvedor).

### <a name="associate-azure-active-directory-with-your-account"></a>Associar Azure Active Directory à sua conta

Para adicionar e gerenciar usuários da conta, você deve primeiro associar sua conta ao Azure Active Directory da sua organização. Se sua organização já usa o Office 365 ou outros serviços comerciais da Microsoft, você já tem Azure AD. Caso contrário, você pode criar um novo locatário do Azure AD sem custo adicional.

Consulte [associar Azure Active Directory à sua conta do Partner Center](/windows/uwp/publish/associate-azure-ad-with-dev-center) para obter mais informações. Embora o tópico se concentre no programa de desenvolvedor de aplicativos do Windows, a associação de um locatário funciona da mesma maneira para o programa de aplicativos da área de trabalho do Windows.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Adicionar usuários, grupos e aplicativos do Azure AD à sua conta

Depois de configurar a associação do Azure AD, você pode adicionar usuários acessando a seção usuários em configurações da conta. Cada usuário recebe uma função que define seu acesso à conta. Você também pode adicionar grupos de usuários e aplicativos do Azure AD para conceder a eles acesso à sua conta do Partner Center. Para obter mais informações sobre como adicionar usuários, consulte [Adicionar usuários, grupos e aplicativos do Azure ad](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

Cada usuário, grupo ou aplicativo do Azure AD que você adiciona à sua conta deve ser atribuído a uma função. Esse processo é descrito em [definir funções ou permissões personalizadas para usuários da conta](/windows/uwp/publish/set-custom-permissions-for-account-users). No entanto, observe que, para o programa de aplicativos da área de trabalho do Windows, não há a capacidade de atribuir permissões personalizadas ou restringir o acesso por produto. Em vez disso, cada usuário deve receber uma das seguintes funções padrão.



| Função      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gerente   | Pode carregar e remover certificados e pode exibir todos os dados analíticos. Tem acesso completo à conta, exceto para alterar informações financeiras. Isso inclui o gerenciamento de usuários, mas observe que a capacidade de criar e excluir usuários no locatário do Azure AD depende da permissão da conta no Azure AD. Ou seja, se uma função de gerente for atribuída a um usuário, mas não tiver permissões de administrador global no Azure AD da organização, elas não poderão criar novos usuários nem excluir usuários do diretório (embora possam alterar a função da conta de um usuário).<br/> Observe que, se sua conta estiver associada a mais de um locatário do Azure AD, um gerente não poderá ver detalhes completos de um usuário (incluindo nome, sobrenome, email de recuperação de senha e se eles são um administrador global do Azure AD), a menos que eles estejam conectados ao mesmo locatário que o usuário com uma conta que tenha permissões de administrador global para esse locatário. No entanto, eles podem adicionar e remover usuários em qualquer locatário associado à conta. <br/> |
| Desenvolvedor | Pode exibir os aplicativos e detalhes de certificado associados à conta e exibir o relatório de **integridade** e **instalações** . Não é possível exibir as informações financeiras ou as configurações de conta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Perguntas frequentes

-   **Por que não vejo nenhum dado para um aplicativo?** Não mostraremos dados até detectarmos usuários suficientes para coletar informações significativas. Se você acabou de lançar seu aplicativo, pode levar algum tempo para atingir esse limite mínimo de adoção. Outro motivo pelo qual você talvez não veja dados é se você não assinou um arquivo com o certificado para um determinado aplicativo. Certifique-se de carregar arquivos assinados com cada certificado que você usa para assinar seus aplicativos.
-   **Posso acessar esses dados por meio de uma API?** Sim, os dados serão disponibilizados por meio de uma API pública quando o programa estiver disponível para todos os desenvolvedores.
-   **E quanto aos aplicativos com certificados mais antigos?** Infelizmente, não há suporte para o envio de certificados expirados ou revogados, mesmo que você os renove com a mesma chave.
-   **Por que vejo um aplicativo que não reconheço?** Se o certificado usado para assinar arquivos em seu aplicativo também for usado por outra pessoa em sua empresa para assinar outro aplicativo, você verá a telemetria para esse aplicativo também. No futuro, forneceremos uma opção para ocultar aplicativos do seu painel. Se a conta da empresa estiver anexada a um locatário do Azure AD, você poderá solicitar que seu administrador modifique as permissões de usuário para que apenas aplicativos específicos fiquem visíveis para você.
-   **Como posso fornecer comentários sobre a experiência ou obter suporte?** Se precisar de assistência, você poderá criar uma solicitação de suporte [aqui](https://developer.microsoft.com/windows/support/). Para compartilhar seus comentários, use o link de **comentários** (em **configurações de conta**) e selecione a área de **análise** para nos informar o que você imagina. 
 

