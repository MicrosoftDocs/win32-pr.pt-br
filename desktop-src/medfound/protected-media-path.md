---
description: 'Este tópico discute três tópicos inter-relacionados: ambiente protegido, gateway de interoperabilidade de mídia e revogação e renovação.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Caminho de mídia protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104553621"
---
# <a name="protected-media-path"></a>Caminho de mídia protegido

Este tópico discute três tópicos inter-relacionados: ambiente protegido, gateway de interoperabilidade de mídia e revogação e renovação.

-   Um PE (ambiente protegido) é um conjunto de tecnologias que permite que o conteúdo protegido flua de e para o Windows Vista de maneira protegida. Todos os componentes dentro de um ambiente protegido são confiáveis e o processo é protegido contra violação.
-   O caminho de mídia protegido (PMP) é um executável que é executado em um ambiente protegido.
-   Se um componente confiável no PE for comprometido, após o processo de conclusão, ele será revogado. No entanto, a Microsoft fornece um mecanismo de renovação para instalar uma versão confiável mais recente do componente quando uma estiver disponível.

Para obter informações sobre componentes de mídia protegidos por assinatura de código, consulte o white paper [assinatura de código para componentes de mídia protegidos no Windows Vista](/windows-hardware/test/hlk/).

Este tópico contém as seguintes seções:

-   [Ambiente protegido](#protected-environment)
-   [Design do ambiente protegido](#design-of-the-protected-environment)
-   [Caminho de mídia protegido](#protected-media-path)
    -   [Autoridades de confiança de entrada](#input-trust-authorities)
    -   [Autoridades de confiança de saída](#output-trust-authorities)
    -   [Objetos de política](#policy-objects)
    -   [Criando objetos no PMP](#creating-objects-in-the-pmp)
-   [Visão geral da negociação de política](#overview-of-policy-negotiation)
-   [Revogação e renovação](#revocation-and-renewal)
-   [Proteção de link de saída](#output-link-protection)
-   [Tópicos relacionados](#related-topics)

## <a name="protected-environment"></a>Ambiente protegido

A proteção de conteúdo abrange várias tecnologias, cada uma delas tentando garantir que o conteúdo não possa ser usado de forma inconsistente com a intenção do proprietário do conteúdo ou do provedor. Essas tecnologias incluem proteção contra cópia, proteção de link, acesso condicional e DRM (gerenciamento de direitos digitais). A base de cada um é confiável: o acesso ao conteúdo é concedido somente a componentes de software que aderem aos termos de uso atribuídos a esse conteúdo.

Para minimizar as ameaças contra o conteúdo protegido, o Windows Vista e o software Media Foundation permitem que o código confiável seja executado em um ambiente protegido. Um PE é um conjunto de componentes, diretrizes e ferramentas projetadas para aumentar a proteção contra pirataria de conteúdo.

Antes de examinar o PE com mais detalhes, é importante entender as ameaças que ele foi projetado para minimizar. Suponha que você esteja executando um aplicativo de mídia em um processo de modo de usuário. O aplicativo é vinculado às várias DLLs (bibliotecas de vínculo dinâmico) que contêm plug-ins de mídia, como decodificadores. Outros processos também estão sendo executados no modo de usuário e vários drivers são carregados no kernel. Se nenhum mecanismo de confiança estiver em vigor, haverá as seguintes ameaças:

-   O aplicativo pode acessar a mídia protegida diretamente ou invadir a memória do processo.
-   Os plug-ins podem acessar o conteúdo diretamente ou invadir a memória do processo.
-   Outros processos podem invadir a memória do processo de mídia diretamente ou injetando código.
-   Os drivers de kernel podem invadir a memória do processo de mídia.
-   O conteúdo pode ser enviado fora do sistema por um meio desprotegido. (A proteção de link foi projetada para mitigar essa ameaça.)

## <a name="design-of-the-protected-environment"></a>Design do ambiente protegido

Um ambiente protegido é executado em um processo protegido separado do aplicativo de mídia. O recurso de processo protegido do Windows Vista impede que outros processos acessem o processo protegido.

Quando um processo protegido é criado, os principais componentes do kernel identificam componentes e plug-ins não confiáveis para que o ambiente protegido possa se recusar a carregá-los. Um componente confiável é aquele que foi assinado adequadamente pela Microsoft. O kernel também controla os módulos que carregam nele, permitindo que o ambiente protegido pare a reprodução do conteúdo protegido se um módulo não confiável for carregado. Antes que um componente de kernel seja carregado, o kernel verifica se ele é confiável. Se não for, os componentes confiáveis que já estão no PE se recusam a processar o conteúdo protegido. Para habilitar isso, os componentes do PE executam periodicamente um handshake protegido criptograficamente com o kernel. Se um componente de modo kernel não confiável estiver presente, o handshake falhará e indicará ao PE que existe um componente não confiável.

Se um componente confiável for comprometido, após o processo de conclusão, ele poderá ser revogado. A Microsoft fornece um mecanismo de renovação para instalar uma versão confiável mais recente, quando disponível.

## <a name="protected-media-path"></a>Caminho de mídia protegido

O caminho de mídia protegido (PMP) é o executável do PE primário para Media Foundation. O PMP é extensível, para que os mecanismos de proteção de conteúdo de terceiros possam ter suporte.

O PMP aceita conteúdo protegido e políticas associadas de qualquer fonte de Media Foundation usando qualquer sistema de proteção de conteúdo, incluindo aqueles fornecidos por terceiros. Ele envia conteúdo para qualquer coletor de Media Foundation, desde que o coletor esteja em conformidade com as políticas especificadas pela origem. Ele também dá suporte a transformações entre a origem e o coletor, incluindo transformações de terceiros, desde que sejam confiáveis.

O PMP é executado em um processo protegido isolado do aplicativo de mídia. O aplicativo só tem a capacidade de trocar mensagens de comando e controle com o PMP, mas não tem acesso ao conteúdo depois que ele é passado para a PMP. O diagrama a seguir ilustra esse processo.

![diagrama do caminho de mídia protegido](images/pmp04.png)

As caixas sombreadas representam componentes que podem ser fornecidos por terceiros. Todos os componentes criados dentro do processo protegido devem ser assinados e confiáveis.

O aplicativo cria uma instância da sessão de mídia dentro do processo protegido e recebe um ponteiro para uma sessão de mídia de proxy, que realiza marshaling de ponteiros de interface no limite do processo.

A origem da mídia pode ser criada dentro do processo do aplicativo, como mostrado aqui ou dentro do processo protegido. Se a origem da mídia for criada dentro do processo do aplicativo, a origem criará um proxy para si mesmo no processo protegido.

Todos os outros componentes de pipeline, como decodificadores e coletores de mídia, são criados no processo protegido. Se esses objetos expõem qualquer interface personalizada para aplicativos, eles devem fornecer um proxy/stub DCOM para realizar marshaling da interface.

Para impor a política no conteúdo protegido conforme ele flui através do pipeline, o PMP usa três tipos de componentes: ITAs (autoridades de confiança de entrada), OTAs (autoridades de confiança de saída) e objetos de política. Esses componentes funcionam em conjunto para conceder ou restringir direitos de uso de conteúdo e para especificar as proteções de link que devem ser empregadas durante a reprodução de conteúdo, como a HDCP (Proteção de Conteúdo Digital de alta largura de banda).

### <a name="input-trust-authorities"></a>Autoridades de confiança de entrada

Um ITA é criado por uma fonte de mídia confiável e executa várias funções:

-   Especifica os direitos para usar o conteúdo. Os direitos podem incluir o direito de reproduzir conteúdo, transferi-lo para um dispositivo e assim por diante. Ele define uma lista ordenada de sistemas de proteção de saída aprovados e as políticas de saída correspondentes para cada sistema. O ITA armazena essas informações em um objeto de política.
-   Fornece o descriptografador necessário para descriptografar o conteúdo.
-   Estabelece uma relação de confiança com o módulo kernel no ambiente protegido, para garantir que o ITA esteja em execução dentro de um ambiente confiável.

Um ITA é associado a um fluxo individual que contém conteúdo protegido. Um fluxo pode ter apenas um ITA, e uma instância de um ITA pode ser associada a apenas um fluxo.

### <a name="output-trust-authorities"></a>Autoridades de confiança de saída

Um OTA é associado a uma saída confiável. O OTA expõe uma ação que a saída confiável pode executar no conteúdo, como reprodução ou cópia. Sua função é impor um ou mais sistemas de proteção de saída exigidos pelo ITA. O OTA consulta o objeto de política fornecido pelo ITA para determinar qual sistema de proteção ele deve impor.

### <a name="policy-objects"></a>Objetos de política

Um objeto de política encapsula os requisitos de proteção de conteúdo de um ITA. Ele é usado pelo mecanismo de política para negociar o suporte à proteção de conteúdo com um OTA. OTAs objetos de política de consulta para determinar quais sistemas de proteção eles devem impor em cada saída do conteúdo atual.

### <a name="creating-objects-in-the-pmp"></a>Criando objetos no PMP

Para criar um objeto no caminho de mídia protegida (PMP), o [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) chama [**IMFPMPHostApp:: ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), com o **IStream** de entrada especificado, formatado da seguinte maneira:

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Visão geral da negociação de política

Há três requisitos fundamentais que devem ser atendidos antes que o conteúdo protegido possa ser processado no PMP. Primeiro, o conteúdo protegido deve ser enviado somente para saídas confiáveis. Segundo, somente as ações permitidas devem ser aplicadas a um fluxo. Terceiro, somente os sistemas de proteção de saída aprovados devem ser usados para reproduzir um fluxo. O mecanismo de política coordena entre ITAs e OTAs para garantir que esses requisitos sejam atendidos.

A maneira mais fácil de entender o processo é percorrer um exemplo simplificado que identifica as etapas necessárias para reproduzir o conteúdo do formato de sistema avançado (ASF) protegido pelo WMDRM (Windows Media Digital Rights Management).

Quando um usuário inicia um aplicativo de Player e abre um arquivo ASF que tem um fluxo de áudio protegido e um fluxo de vídeo protegido, as seguintes etapas devem ser executadas:

1.  O aplicativo cria a origem de mídia do ASF e a sessão do PMP (caminho de mídia protegida). Media Foundation cria um processo de PMP.
2.  O aplicativo cria uma topologia parcial que contém um nó de fonte de áudio conectado ao processador de áudio e um nó de fonte de vídeo conectado ao processador de vídeo avançado (EVR). Para os renderizadores, o aplicativo não cria diretamente o renderizador. Em vez disso, o aplicativo cria no processo desprotegido um objeto conhecido como um *objeto de ativação*. O PMP usa o objeto de ativação para criar os renderizadores no processo protegido. (Para obter mais informações sobre objetos de ativação, consulte [objetos de ativação](activation-objects.md).)
3.  O aplicativo define a topologia parcial na sessão do PMP.
4.  A sessão do PMP serializa a topologia e a transmite para o host do PMP no processo protegido. O host do PMP envia a topologia para o mecanismo de política.
5.  O carregador de topologia chama [**IMFInputTrustAuthority:: Getdescriptografar**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) no ITAs e insere os descriptografadores na topologia imediatamente downstream dos nós de origem correspondentes.
6.  O carregador de topologia insere os decodificadores de áudio e vídeo downstream dos nós Decrypter.
7.  O mecanismo de política examina os nós inseridos para determinar se qualquer implementação da interface [**IMFTrustedOutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) . O EVR e o processador de áudio implementam **IMFTrustedOutput**, pois eles enviam dados fora do PMP.
8.  Cada ITA confirma que está sendo executado dentro de um processo protegido executando um handshake criptográfico com um módulo de kernel do ambiente protegido.
9.  Para cada fluxo, o mecanismo de política negocia a política obtendo um objeto de política do ITA e passando-o para o OTA. O OTA fornece uma lista dos sistemas de proteção que ele suporta e o objeto de política indica quais sistemas de proteção devem ser aplicados, juntamente com as configurações corretas. Em seguida, o OTA aplica essas configurações. Se ele não puder fazer isso, o conteúdo será bloqueado.

## <a name="revocation-and-renewal"></a>Revogação e renovação

Um componente confiável pode ser revogado se for comprometido ou for descoberto que está violando os contratos de licença sob os quais ele foi inicialmente confiável. Existe um mecanismo de renovação para instalar uma versão mais recente e mais confiável do componente.

Os componentes confiáveis são assinados usando um certificado criptográfico. A Microsoft publica uma lista de revogação global (GRL) que identifica os componentes que foram revogados. O GRL é assinado digitalmente para garantir sua autenticidade. Os proprietários de conteúdo podem garantir, por meio do mecanismo de política, que a versão atual do GRL está presente no computador do usuário.

## <a name="output-link-protection"></a>Proteção de link de saída

Quando o conteúdo de vídeo Premium é exibido, os quadros descriptografados e descompactados viajam através de um conector físico para o dispositivo de vídeo. Os provedores de conteúdo podem exigir que os quadros de vídeo sejam protegidos neste ponto, à medida que viajam pelo conector físico. Existem vários mecanismos de proteção para essa finalidade, incluindo High-Bandwidth Proteção de Conteúdo Digital (HDCP) e Proteção de Conteúdo DisplayPort (DPCP). O vídeo OTA impõe essas proteções usando o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM). O Gerenciador de proteção de saída envia comandos para o driver de gráficos e o driver de gráficos impõe quaisquer mecanismos de proteção de link exigidos pela política.

![um diagrama que mostra a relação entre o vídeo OTA e o OPM.](images/pmp05.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> <dt>

[Sessão de mídia do PMP](pmp-media-session.md)
</dt> </dl>

 

 
