---
description: 'Saiba mais sobre: usando o Gerenciador de proteção de saída'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Usando o Gerenciador de proteção de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e37dd548603a6f9d7769a9e724df3477e2fcde
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475512"
---
# <a name="using-output-protection-manager"></a>Usando o Gerenciador de proteção de saída

Este tópico descreve como usar o OPM (Gerenciador de proteção de saída) para proteger o conteúdo de vídeo conforme ele viaja em um conector físico para um dispositivo de vídeo. Este tópico contém as seguintes seções:

-   [Saídas de vídeo](#video-outputs)
-   [Inicializando uma sessão OPM](#initializing-an-opm-session)
-   [Enviando solicitações de status OPM](#sending-opm-status-requests)
-   [Enviando comandos OPM](#sending-opm-commands)
-   [Manipulando uma saída de vídeo desabilitada](#sending-opm-commands)
-   [Usando o HDCP para proteger o conteúdo](#using-hdcp-to-protect-content)

Premium conteúdo de vídeo geralmente é criptografado para protegê-lo contra duplicação não autorizada. É claro que o vídeo deve ser descriptografado antes de ser exibido. Os quadros descriptografados e descompactados devem viajar por um conector físico para o dispositivo de vídeo. Os provedores de conteúdo podem exigir que os quadros de vídeo sejam protegidos neste ponto, à medida que viajam pelo conector físico.

Existem vários mecanismos de proteção para essa finalidade, incluindo High-Bandwidth Proteção de Conteúdo Digital (HDCP) e Proteção de Conteúdo de DisplayPort (DPCP) para saídas digitais; e sistema de gerenciamento de geração de cópia – analógico (CGMS-A) para saídas analógicas. Em geral, esses mecanismos envolvem criptografar ou embaralhar o sinal antes que ele vá para a tela.

OPM permite que um aplicativo aplique mecanismos de proteção de conteúdo na saída de vídeo. Usando OPM, o aplicativo envia comandos e solicitações de status para o driver de gráficos por meio de um canal confiável e seguro. OPM permite que um aplicativo:

-   Verifique se um driver de gráficos foi assinado pela Microsoft.
-   Configure um canal de comunicação confiável com o driver.
-   Impor mecanismos de proteção de conteúdo na saída física.

OPM substitui a Border de proteção de saída certificada (COPP) e usa uma API semelhante. Para compatibilidade com versões anteriores, a interface OPM pode emular a interface COPP. As diferenças entre OPM e COPP incluem o seguinte:

-   OPM usa certificados X. 509, enquanto COPP usa um formato de certificado proprietário.
-   OPM dá suporte a repetidores de HDCP.
-   Os aplicativos que usam OPM não precisam analisar SRMs (mensagens de renovação do sistema HDCP).
-   Os OPM podem ser usados quando a exibição de gráficos estiver usando o modo de clonagem. A COPP não oferece suporte ao modo de clonagem.

Se seu aplicativo usar o caminho de mídia protegido (PMP) para reproduzir conteúdo de vídeo, você não precisará usar a API OPM, pois o PMP faz todas as chamadas OPM necessárias. A API OPM está disponível para aplicativos que não usam o PMP.

o OPM está disponível no Windows Vista e posterior, mas a API não foi disponibilizada até Windows 7. para usar o OPM em um aplicativo, você deve ter os cabeçalhos e os arquivos de biblioteca do SDK do Windows 7. você não precisa redistribuir nenhuma dll para usar o OPM no Windows Vista ou no Windows Server 2008.

## <a name="video-outputs"></a>Saídas de vídeo

Um adaptador gráfico pode ter mais de uma saída física, cada uma com seus próprios recursos. Antes que um aplicativo Reproduza conteúdo protegido, ele deve definir os mecanismos de proteção apropriados em cada saída de vídeo associada à placa gráfica que exibirá o vídeo. Quais mecanismos de proteção serão aplicados dependerão das regras de uso do conteúdo.

Cada saída de vídeo é representada por uma instância da interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Você pode usar um dispositivo Direct3D ou identificadores de monitor para obter as saídas de vídeo.

Usando um dispositivo Direct3D:

1.  Obtenha o ponteiro **IDirect3DDevice9** para o dispositivo Direct3D que seu aplicativo usará para criar superfícies para manter os quadros de vídeo.
2.  Chame a função [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) . Essa função aloca uma matriz de ponteiros [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uma para cada saída.

Usando identificadores de monitor:

1.  Chame **EnumDisplayMonitors** para obter os identificadores de **HMONITOR** que correspondem à janela de vídeo. Vários monitores podem ser associados à mesma janela, portanto, você pode obter vários identificadores de **HMONITOR** .
2.  Para cada identificador de monitor, chame [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Essa função aloca uma matriz de ponteiros [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uma para cada saída.

## <a name="initializing-an-opm-session"></a>Inicializando uma sessão OPM

Antes que o aplicativo envie comandos OPM ou solicitações de status, ele deve verificar se a saída do vídeo é confiável e estabelecer uma chave de sessão. A chave de sessão é usada para assinar os dados trocados entre o aplicativo e o driver de gráficos.

A API OPM define um handshake que estabelece confiança e define a chave de sessão. Você deve executar esse handshake para cada instância da interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , da seguinte maneira:

1.  Chame [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Esse método recupera duas partes de dados:
    -   Um número aleatório, gerado pelo driver. Você usará esse número para concluir o handshake.
    -   A cadeia de certificados X. 509 do driver.
2.  Verifique se a cadeia de certificados foi assinada pela Microsoft.
    > [!Note]  
    > A revogação de certificado está fora do escopo de OPM.

     

3.  Obtenha a chave pública do driver da cadeia de certificados.
4.  Gere uma chave de sessão AES de 128 bits.
5.  Gere dois números aleatórios de 32 bits:

    -   O número de sequência inicial para solicitações de status OPM.
    -   O número de sequência inicial para comandos OPM.

    Esses números devem ser gerados usando um gerador de números pseudo aleatórios criptograficamente seguro, como **CryptGenRandom**.

6.  Copie o número aleatório do driver (obtido na etapa 1), a chave de sessão e os dois números de sequência em uma estrutura de [**\_ \_ \_ parâmetros de inicialização criptografada em OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) , conforme descrito em [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Criptografe a estrutura de [**\_ parâmetros de \_ inicialização \_ de OPM ENCRYPTED**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) com RSAES-OAEP, usando a chave pública do driver, que é encontrada no certificado do driver.
8.  Chame [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Enviando solicitações de status OPM

As solicitações de status OPM retornam informações sobre a saída de vídeo, como o tipo de conector físico e o nível de proteção atual. Para obter uma lista de tipos de solicitação, consulte [solicitações de status OPM](opm-status-requests.md).

Para enviar uma solicitação de status, execute as etapas a seguir.

1.  Inicialize uma estrutura de [**\_ \_ \_ parâmetros obter informações de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) , conforme mostrado na tabela a seguir.

    | Membro               | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**             | Ignore este campo por enquanto.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Um número aleatório de 128 bits segura criptograficamente seguro. Sempre que você fizer uma solicitação de status, sempre gere um novo número aleatório, mesmo se você estiver fazendo a mesma solicitação. Armazene o número em uma variável, pois será necessário consultá-lo mais tarde.                                                                                                                             |
    | **guidInformation**  | Um GUID que identifica a solicitação de status. Para obter uma lista de solicitações de status, consulte [solicitações de status OPM](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | O número de sequência. Para a primeira solicitação de status, use o número de sequência inicial que você especificou no método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (etapa 5 da [inicialização de uma sessão OPM](#initializing-an-opm-session).) Cada vez que você fizer outra solicitação de status, aumente esse número em 1. |
    | **abParameters**     | Uma matriz de bytes que contém dados de entrada adicionais para a solicitação. O formato dos dados de entrada é listado no tópico de referência para cada solicitação de status.                                                                                                                                                                                                                    |
    | **cbParametersSize** | O tamanho dos dados válidos na matriz **abParameters** . O conteúdo do restante da matriz é indefinido.                                                                                                                                                                                                                                                              |

    

     

2.  Calcule o OMAC-1 do CBC de chave para calcular um hash para o bloco de dados que aparece após o membro **OMAC** e, em seguida, defina o membro **OMAC** com esse valor. Consulte [código de exemplo OPM](opm-example-code.md).
3.  Chame o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) . Passe um ponteiro para a estrutura [**\_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) do OPM e um ponteiro para uma estrutura DE INFORMAÇÕES [**\_ SOLICITADAS \_ do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) A resposta do driver é escrita na estrutura **\_ OPM REQUESTED \_ INFORMATION.**
    -   O **membro omac** dessa estrutura contém um OMAC computado para os dados que seguem esse membro.
    -   O **membro abRequestedInformation é** uma matriz de byte que contém dados de saída para a resposta. O formato dos dados de saída é listado no tópico de referência para cada solicitação de status.
4.  Calcule um OMAC para a [**estrutura \_ OPM REQUESTED \_ INFORMATION,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) não incluindo **o membro omac.** Verifique se o OMAC corresponde ao valor no **membro omac.**
5.  Certifique-se de que o membro **cbRequestedInformationSize** da estrutura [**\_ OPM REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) fornece o tamanho correto para os dados de saída. Por exemplo, os dados de saída para a consulta [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md) são uma estrutura de INFORMAÇÕES PADRÃO do [**OPM, \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) portanto, o valor **de cbRequestedInformationSize** deve ser `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Caste **o membro abRequestedInformation da** estrutura [**\_ OPM REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) para a estrutura de dados de saída correta. Por exemplo, se a solicitação de status for [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md), cast **abRequestedInformation** em uma [**estrutura de INFORMAÇÕES PADRÃO \_ \_ do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
7.  Certifique-se **de que o membro rnRandomNumber** da estrutura de dados de saída corresponde ao valor de **rnRandomNumber** da etapa 1.
8.  Verifique o **membro ulStatusFlags** da estrutura de dados de saída, conforme descrito em Manipulando [uma saída de vídeo desabilitada.](#handling-a-disabled-video-output)

Se qualquer uma das verificações nas etapas 5 a 8 falhar, o aplicativo deverá parar de mostrar o conteúdo protegido.

## <a name="sending-opm-commands"></a>Enviando comandos OPM

Comandos OPM são usados para definir o nível de proteção e outras configurações na saída do vídeo. Enviar um comando OPM é semelhante ao envio de uma solicitação de status, exceto que não há dados de resposta do driver. Para ver uma lista de comandos, consulte [Comandos OPM](opm-commands.md).

Para enviar um comando OPM, execute as etapas a seguir.

1.  Preencha uma estrutura [**CONFIGURE \_ \_ PARAMETERS do OPM,**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) conforme mostrado na tabela a seguir.

    | Membro                | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | Ignore esse campo por enquanto.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | Um GUID que identifica o comando. Para ver uma lista de comandos, consulte [Comandos OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | O número de sequência. Para o primeiro comando, use o número de sequência inicial que você especificou no método [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (etapa 5 de Inicializando uma sessão [OPM](#initializing-an-opm-session).) Sempre que você enviar outro comando, incremente esse número em 1. |
    | **abParameters**      | Uma matriz de byte que contém dados de entrada adicionais para o comando. O formato dos dados de entrada é listado no tópico de referência para cada comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | O tamanho dos dados válidos na **matriz abParameters.** O conteúdo do restante da matriz é indefinido.                                                                                                                                                                                                                                                |

    

     

2.  Calcule um OMAC para o bloco de dados que aparece após o membro **omac** e, em seguida, de definir o **membro omac** para esse valor.
3.  Chame [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Para a maioria dos comandos, há uma solicitação de status correspondente que retorna o status do comando. Por exemplo, o [**comando OPM \_ SET PROTECTION \_ \_ LEVEL**](opm-set-protection-level.md) define o nível de proteção e o comando GET VIRTUAL PROTECTION [**\_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) do OPM obtém o nível de proteção atual.

## <a name="handling-a-disabled-video-output"></a>Manipulando uma saída de vídeo desabilitada

Uma saída de vídeo pode se desabilitar a qualquer momento para impedir o uso não autorizado de conteúdo de vídeo. Isso pode ocorrer porque um mecanismo de proteção para de funcionar, porque o driver detecta adulteração ou porque a exibição foi desconectada do conector físico. Enquanto uma saída de vídeo está desabilitada, nenhum quadro de vídeo é exibido.

Embora a proteção de conteúdo seja habilitada, um aplicativo deve executar periodicamente (pelo menos uma vez a cada 2 segundos) as etapas a seguir.

1.  Chame [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) para enviar a solicitação de status [**GET ACTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-actual-protection-level.md) ou [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL.**](opm-get-virtual-protection-level.md) Os dados de retorno para ambos os comandos são uma [**estrutura OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
2.  Verifique o **membro ulInformation** da estrutura [**OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Esse membro contém um sinalizador que indica se a proteção de conteúdo ainda está habilitada. Se a proteção de conteúdo estiver desligada, pare de tocar o vídeo imediatamente.
3.  Se a proteção de conteúdo estiver em, verifique **o membro ulStatusFlags** da estrutura [**OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Se nenhum sinalizador for definido, a saída do vídeo funcionará corretamente. Caso contrário, a saída do vídeo será desabilitada.

Os sinalizadores a seguir são definidos **para ulStatusFlags**.




| Sinalizador | Descrição | 
|------|-------------|
| <strong>OPM_STATUS_LINK_LOST</strong> | A proteção de saída parou de funcionar por algum motivo; por exemplo, o dispositivo de exibição pode ser desconectado do conntector. Pare a reprodução e desligue todos os mecanismos de proteção de saída. | 
| <strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong> | O aplicativo deve restabelecer a sessão do OPM. Responda da seguinte forma:<ol><li>Pare a reprodução.</li><li>Desligue todos os mecanismos de proteção.</li><li>Libere a <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>interface IOPMVideoOutput.</strong></a></li><li>Recrie todas as superfícies de vídeo.</li><li>Crie um novo objeto OPM e tente restabelecer a proteção de conteúdo. Se isso falhar, exibirá uma mensagem de erro para o usuário. Não reproduza mais conteúdo de vídeo.</li></ol> | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Esse sinalizador se aplica somente quando o HDCP é usado e indica a presença de um dispositivo HDCP revogado. Pare a reprodução e desligue todos os mecanismos de proteção nesta saída de vídeo. Quando esse sinalizador é definido, o <strong>sinalizador OPM_STATUS_LINK_LOST</strong> também é definido. | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | O driver detectou adulteração. Pare a reprodução e não reproduza mais nenhum vídeo usando essa saída de vídeo. Também é uma boa ideia parar de usar outras saídas de vídeo, pois o sistema pode estar comprometido. | 




 

## <a name="using-hdcp-to-protect-content"></a>Usando o HDCP para proteger o conteúdo

Esta seção descreve como habilitar a proteção de saída HDCP usando o OPM. Aqui está uma delineia geral das etapas que o aplicativo deve seguir. Detalhes são dados posteriormente nesta seção.

1.  O aplicativo pode ter que fornecer um SRM para a saída de vídeo. O mecanismo para receber SRMs está fora do escopo da interface OPM. Por exemplo, SRMs podem ser entregues como parte de um fluxo de difusão.
2.  O aplicativo habilita a proteção de saída HDCP.
3.  O aplicativo reproduz o conteúdo do vídeo. Periodicamente, o aplicativo sonda o driver para verificar se o HDCP está.
4.  Quando a reprodução for concluída, o aplicativo desligará o HDCP.

### <a name="setting-the-srm"></a>Definindo o SRM

Para definir o SRM, execute as etapas a seguir.

1.  Inicialize uma [**estrutura OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) com o número de versão srm.
2.  Armazene o SRM em uma variável.
3.  Envie um [**comando OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) para a saída de vídeo. Use o procedimento descrito em [Enviando comandos OPM.](#sending-opm-commands)
    -   O **membro abParameters** da estrutura [**OPM CONFIGURE \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contém a estrutura [**OPM SET \_ \_ HDCP \_ SRM \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)
    -   O *parâmetro pbAdditionalParameters* do método [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) aponta para a variável que contém o SRM.
4.  Envie uma solicitação de status DO [**\_ \_ \_ OPM GET CURRENT HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md) para a saída do vídeo. Use o procedimento descrito em [Enviando solicitações de status do OPM.](#sending-opm-status-requests) Essa solicitação de status não tem dados de entrada, portanto, o conteúdo do membro **abParameters** da estrutura [**GET INFO \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) do OPM é indefinido.
5.  Quando o [**método IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorna, a matriz **abRequestedInformation** na estrutura [**\_ OPM REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contém uma estrutura [**OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) O membro **ulInformation** dessa estrutura contém o número de versão do SRM atual. Esse valor deve ser igual ao valor da etapa 2.

### <a name="enabling-hdcp"></a>Habilitando HDCP

Para habilitar o HDCP, execute as etapas a seguir.

1.  Inicialize uma estrutura de [**parâmetros de nível de proteção dos OPMS \_ definidos \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) com os seguintes valores:
    -   **ulProtectionType**  =  **OPM \_ tipo de proteção de \_ \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ ativado**
    -   **Reservado** = 0
    -   **Reserved2** = 0
2.  Envie um [**comando \_ OPM \_ definir \_ nível de proteção**](opm-set-protection-level.md) . Os dados de entrada na matriz **abParameters** são a estrutura de parâmetros de [**nível de proteção de OPM \_ definido \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .
3.  Envie uma solicitação de status de erro de [**\_ \_ \_ \_ nível de proteção virtual OPM**](opm-get-virtual-protection-level.md) para verificar se o HDCP está habilitado. Os quatro primeiros bytes do membro **abParameters** da estrutura de [**\_ parâmetros get \_ info \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contêm o valor de **\_ proteção OPM \_ tipo \_ HDCP**.

Quando o método [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorna, a matriz **abRequestedInformation** na estrutura [**de \_ \_ informações de OPM solicitado**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contém uma estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O membro **ulInformation** dessa estrutura contém um valor da enumeração de [**\_ \_ \_ nível de proteção de HDCP de OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) . Se o valor for igual a **OPM \_ HDCP \_ em**, significa que HDCP está habilitado. Caso contrário, repita as etapas 1 a 2 até que a HDCP esteja habilitada ou um erro ocorra. (Lembre-se de incrementar o número de sequência e gerar um novo número aleatório a cada vez.)

Geralmente leva entre 100 e 200 milissegundos para habilitar a HDCP, mas pode levar mais tempo. Não presuma que o HDCP esteja habilitado até que você o tenha verificado.

Quando o aplicativo terminar de reproduzir o conteúdo protegido, desative o HDCP. As etapas são as mesmas para habilitar a HDCP, mas na etapa 1, defina **ulProtectionLevel** como **OPM de \_ HDCP \_ desativado**.

> [!Note]  
> Não habilite HDCP se o tipo de conector for um **\_ tipo de conector OPM \_ \_ DisplayPort \_ incorporado**. (Consulte [**sinalizadores de tipo de conector OPM**](opm-connector-type-flags.md).)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 



