---
description: 'Saiba mais sobre: usando o Gerenciador de proteção de saída'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Usando o Gerenciador de proteção de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bf4def3b0575dd706ae5f0c62924b6f1375a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795470"
---
# <a name="using-output-protection-manager"></a>Usando o Gerenciador de proteção de saída

Este tópico descreve como usar o OPM (Gerenciador de proteção de saída) para proteger o conteúdo de vídeo conforme ele viaja em um conector físico para um dispositivo de vídeo. Este tópico contém as seguintes seções:

-   [Saídas de vídeo](#video-outputs)
-   [Inicializando uma sessão OPM](#initializing-an-opm-session)
-   [Enviando solicitações de status OPM](#sending-opm-status-requests)
-   [Enviando comandos OPM](#sending-opm-commands)
-   [Manipulando uma saída de vídeo desabilitada](#sending-opm-commands)
-   [Usando o HDCP para proteger o conteúdo](#using-hdcp-to-protect-content)

O conteúdo de vídeo Premium geralmente é criptografado para protegê-lo contra duplicação não autorizada. É claro que o vídeo deve ser descriptografado antes de ser exibido. Os quadros descriptografados e descompactados devem viajar por um conector físico para o dispositivo de vídeo. Os provedores de conteúdo podem exigir que os quadros de vídeo sejam protegidos neste ponto, à medida que viajam pelo conector físico.

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

O OPM está disponível no Windows Vista e versões posteriores, mas a API não foi feita em público até o Windows 7. Para usar o OPM em um aplicativo, você deve ter os cabeçalhos e os arquivos de biblioteca do SDK do Windows 7. Você não precisa redistribuir nenhuma dll para usar o OPM no Windows Vista ou no Windows Server 2008.

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
3.  Chame o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) . Passe um ponteiro para a estrutura [**de \_ \_ \_ parâmetros Get Info de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) e um ponteiro para uma estrutura de [**\_ \_ informações solicitada em OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) . A resposta do driver é gravada na estrutura de **\_ \_ informações de OPM solicitado** .
    -   O membro **OMAC** dessa estrutura contém um OMAC computado para os dados que seguem esse membro.
    -   O membro **abRequestedInformation** é uma matriz de bytes que contém os dados de saída para a resposta. O formato dos dados de saída é listado no tópico de referência para cada solicitação de status.
4.  Calcule um OMAC para a estrutura de [**\_ \_ informações de OPM solicitado**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) , não incluindo o membro **OMAC** . Verifique se OMAC corresponde ao valor no membro **OMAC** .
5.  Verifique se o membro **cbRequestedInformationSize** da estrutura [**de \_ \_ informações requeridas de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) fornece o tamanho correto para os dados de saída. Por exemplo, os dados de saída para a consulta de [**tipo de conector do OPM \_ \_ \_ Get**](opm-get-connector-type.md) são uma estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) , portanto, o valor de **cbRequestedInformationSize** deve ser `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Converta o membro **abRequestedInformation** da estrutura de [**informações de OPM \_ solicitada \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) na estrutura de dados de saída correta. Por exemplo, se a solicitação de status [**for \_ \_ \_ tipo de conector de obtenção de OPM**](opm-get-connector-type.md), converta **abRequestedInformation** em uma estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
7.  Verifique se o membro **rnRandomNumber** da estrutura de dados de saída corresponde ao valor de **rnRandomNumber** da etapa 1.
8.  Verifique o membro **ulStatusFlags** da estrutura de dados de saída, conforme descrito em [lidando com uma saída de vídeo desabilitada](#handling-a-disabled-video-output).

Se qualquer uma das verificações nas etapas 5 a 8 falhar, o aplicativo deverá parar de mostrar o conteúdo protegido.

## <a name="sending-opm-commands"></a>Enviando comandos OPM

Os comandos OPM são usados para definir o nível de proteção e outras configurações na saída de vídeo. O envio de um comando OPM é semelhante ao envio de uma solicitação de status, exceto que não há dados de resposta do driver. Para obter uma lista de comandos, consulte [comandos OPM](opm-commands.md).

Para enviar um comando OPM, execute as etapas a seguir.

1.  Preencha uma estrutura [**de \_ configuração de \_ parâmetros de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) , conforme mostrado na tabela a seguir.

    | Membro                | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | Ignore este campo por enquanto.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | Um GUID que identifica o comando. Para obter uma lista de comandos, consulte [comandos OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | O número de sequência. Para o primeiro comando, use o número de sequência inicial que você especificou no método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (etapa 5 de [inicialização de uma sessão OPM](#initializing-an-opm-session).) Cada vez que você enviar outro comando, aumente esse número em 1. |
    | **abParameters**      | Uma matriz de bytes que contém dados de entrada adicionais para o comando. O formato dos dados de entrada é listado no tópico de referência para cada comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | O tamanho dos dados válidos na matriz **abParameters** . O conteúdo do restante da matriz é indefinido.                                                                                                                                                                                                                                                |

    

     

2.  Calcule um OMAC para o bloco de dados que aparece após o membro **OMAC** e, em seguida, defina o membro **OMAC** como esse valor.
3.  Chame [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Para a maioria dos comandos, há uma solicitação de status correspondente que retorna o status do comando. Por exemplo, o comando de [**\_ Configurar \_ \_ nível de proteção OPM**](opm-set-protection-level.md) define o nível de proteção e o comando [**OPM \_ obter \_ \_ \_ nível de proteção virtual**](opm-get-virtual-protection-level.md) Obtém o nível de proteção atual.

## <a name="handling-a-disabled-video-output"></a>Manipulando uma saída de vídeo desabilitada

Uma saída de vídeo pode ser desativada a qualquer momento para evitar o uso não autorizado de conteúdo de vídeo. Isso pode ocorrer porque um mecanismo de proteção para de funcionar, pois o driver detecta violação ou porque a tela foi desconectada do conector físico. Enquanto uma saída de vídeo está desabilitada, nenhum quadro de vídeo é exibido.

Enquanto a proteção de conteúdo está habilitada, um aplicativo deve periodicamente (pelo menos uma vez a cada 2 segundos) para executar as etapas a seguir.

1.  Chame [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) para enviar a solicitação de status do [**OPM \_ obter \_ \_ \_ nível de proteção real**](opm-get-actual-protection-level.md) ou [**OPM \_ obter \_ \_ \_ nível de proteção virtual**](opm-get-virtual-protection-level.md) . Os dados de retorno de ambos os comandos são uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
2.  Verifique o membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Esse membro contém um sinalizador que indica se a proteção de conteúdo ainda está habilitada. Se a proteção de conteúdo estiver desativada, pare de executar o vídeo imediatamente.
3.  Se a proteção de conteúdo estiver ativada, verifique o membro **ulStatusFlags** da estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Se nenhum sinalizador for definido, a saída de vídeo estará funcionando corretamente. Caso contrário, a saída de vídeo será desabilitada.

Os sinalizadores a seguir são definidos para **ulStatusFlags**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sinalizador</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>OPM_STATUS_LINK_LOST</strong></td>
<td>A proteção de saída parou de funcionar por algum motivo; por exemplo, o dispositivo de vídeo pode ser desconectado do conntector. Pare a reprodução e desative todos os mecanismos de proteção de saída.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></td>
<td>O aplicativo deve restabelecer a sessão OPM. Responda da seguinte maneira:
<ol>
<li>Pare a reprodução.</li>
<li>Desative todos os mecanismos de proteção.</li>
<li>Libere a interface <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> .</li>
<li>Recrie todas as superfícies de vídeo.</li>
<li>Crie um novo objeto OPM e tente restabelecer a proteção de conteúdo. Se isso falhar, exiba uma mensagem de erro para o usuário. Não reproduza mais conteúdo de vídeo.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Esse sinalizador se aplica somente quando HDCP é usado e indica a presença de um dispositivo HDCP revogado. Pare a reprodução e desative todos os mecanismos de proteção nesta saída de vídeo. Quando esse sinalizador é definido, o sinalizador de <strong>OPM_STATUS_LINK_LOST</strong> também é definido.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>O driver detectou violação. Pare a reprodução e não reproduza mais vídeo usando esta saída de vídeo. Também é uma boa ideia parar de usar qualquer outra saída de vídeo, pois o sistema pode estar comprometido.</td>
</tr>
</tbody>
</table>



 

## <a name="using-hdcp-to-protect-content"></a>Usando o HDCP para proteger o conteúdo

Esta seção descreve como habilitar a proteção de saída de HDCP usando OPM. Aqui está uma descrição geral das etapas que o aplicativo deve executar. Os detalhes são fornecidos posteriormente nesta seção.

1.  O aplicativo pode precisar fornecer um SRM para a saída de vídeo. O mecanismo para o recebimento de SRMs está fora do escopo da interface OPM. Por exemplo, SRMs pode ser entregue como parte de um fluxo de difusão.
2.  O aplicativo habilita a proteção de saída de HDCP.
3.  O aplicativo reproduz o conteúdo do vídeo. Periodicamente, o aplicativo sonda o driver para verificar se o HDCP está ativado.
4.  Quando a reprodução é concluída, o aplicativo desativa HDCP.

### <a name="setting-the-srm"></a>Configurando o SRM

Para definir o SRM, execute as etapas a seguir.

1.  Inicialize uma estrutura de [**\_ parâmetros de \_ \_ SRM \_ de HDCP definido de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) com o número de versão do SRM.
2.  Armazene o SRM em uma variável.
3.  Envie um comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) para a saída de vídeo. Use o procedimento descrito em [enviando comandos OPM](#sending-opm-commands).
    -   O membro **abParameters** da estrutura [**de \_ Configurar \_ parâmetros de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contém a estrutura de [**\_ \_ \_ \_ parâmetros de SRM de HDCP definido**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) .
    -   O parâmetro *pbAdditionalParameters* do método [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) aponta para a variável que contém o SRM.
4.  Envie um OPM para obter a solicitação de status de [**\_ versão de \_ \_ \_ SRM \_ de HDCP atual**](opm-get-current-hdcp-srm-version.md) para a saída de vídeo. Use o procedimento descrito em [enviando solicitações de status OPM](#sending-opm-status-requests). Essa solicitação de status não tem dados de entrada, portanto, o conteúdo do membro **abParameters** da estrutura de [**\_ \_ \_ parâmetros Get Info de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) não está definido.
5.  Quando o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorna, a matriz **abRequestedInformation** na estrutura [**de \_ \_ informações de OPM solicitado**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contém uma estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . O membro **ulInformation** dessa estrutura contém o número de versão do SRM atual. Esse valor deve ser igual ao valor da etapa 2.

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

 

 



