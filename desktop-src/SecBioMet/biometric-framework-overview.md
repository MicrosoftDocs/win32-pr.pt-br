---
title: Visão geral da estrutura biométrica
description: O suporte nativo para dispositivos biométricos é incorporado ao Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454214"
---
# <a name="biometric-framework-overview"></a>Visão geral da estrutura biométrica

Cada indivíduo tem características exclusivas que podem ser usadas para identificação. Normalmente, essas características são físicas e incluem características como impressões digitais, mas também podem incluir características comportamentais, como da e digitar ritmo. O termo biometria abrange ambos os significados. As informações biométricas estão substituindo cada vez mais as senhas para identificar e verificar os usuários. Ele é mais seguro e, muitas vezes, mais conveniente para o usuário e o administrador.

Os sensores são usados para capturar informações biométricas. As informações são capturadas pelo sensor como um exemplo biométrico. Um único exemplo contém dados que representam uma característica biométrica única para um indivíduo. São calculadas várias amostras para criar um modelo biométrico e o modelo é armazenado com segurança. Posteriormente, um exemplo de um usuário desconhecido é comparado aos modelos armazenados para estabelecer e verificar a identidade do usuário. O serviço biométrico do Windows, parte do Windows Biometric Framework (WBF), fornece a funcionalidade a seguir. Você pode usar a API do Windows Biometric Framework para otimizar essa funcionalidade.

-   Captura amostras biométricas e as utiliza para criar um modelo.
-   Salva e recupera modelos biométricos com segurança.
-   Mapeia cada modelo para um identificador exclusivo, como um GUID ou um SID.

Você também pode usar essa API para estender a estrutura e criar adaptadores de sensor biométrico, mecanismos de correspondência e componentes de armazenamento. Para obter mais informações sobre como criar adaptadores de sensor, mecanismos correspondentes e componentes de armazenamento, consulte [criando plug-ins de adaptador](creating-adapter-plug-ins.md).

## <a name="core-platform-components"></a>Componentes da plataforma principal

### <a name="windows-biometric-driver-interface-wbdi"></a>WBDI (Windows Biometric Driver Interface)

WBDI é uma interface de programação que um driver biométrico pode usar para expor o dispositivo biométrico por meio do serviço de biometria do Windows (EDT). Você pode implementar um driver WBDI usando qualquer tecnologia de driver com suporte, incluindo o seguinte. No entanto, recomendamos que você use o UMDF quando possível para melhorar a qualidade do driver e a estabilidade do sistema.

-   Estrutura de driver de modo de usuário (UMDF)
-   Estrutura de driver de modo kernel (KMDF)
-   Windows Driver Model (WDM)

Um driver biométrico WBDI também deve oferecer suporte ao GUID da interface do driver WBDI e a todos os controles de e/s obrigatórios (IOCTLs). Os desenvolvedores de driver devem examinar a documentação e o código de exemplo no WDK (Kit de driver do Windows).

### <a name="windows-biometric-service-wbs"></a>Serviço biométrico do Windows (EDT)

O serviço de biometria do Windows gerencia drivers biométricos instalados e dá suporte à API de Windows Biometric Framework para fornecer acesso de dispositivo a aplicativos cliente. A EDT executa as seguintes funções:

-   Ele protege a confidencialidade do usuário separando aplicativos cliente de dados biométricos.
-   Ele protege dados biométricos de aplicativos cliente sem privilégios, exigindo que os aplicativos tenham acesso aos dados usando identificadores exclusivos.
-   Ele usa um componente de software chamado [unidade biométrica](/previous-versions//dd401512(v=vs.85)) para expor os recursos de um dispositivo biométrico específico por meio de uma interface padronizada.
-   Ele gerencia unidades biométricas agrupando-as em [pools de sensores](sensor-pools.md)do sistema, privados ou não atribuídos.
-   Ele dá suporte ao uso de [adaptadores](/previous-versions//dd401508(v=vs.85)) de unidade biométrico para dispositivos físicos que não possuem recursos de processamento ou armazenamento integrados.

### <a name="windows-biometric-framework-api"></a>API do Windows Biometric Framework

A API Windows Biometric Framework permite que você crie aplicativos cliente que podem interagir com o serviço biométrico do Windows para executar as seguintes ações:

-   Identificar e verificar usuários.
-   Localize dispositivos biométricos e consulte seus recursos.
-   Gerenciar sessões e monitorar eventos.

## <a name="user-experience-components"></a>Componentes de experiência do usuário

### <a name="discovery-points"></a>Pontos de descoberta

Os usuários finais podem localizar dispositivos biométricos por qualquer um dos seguintes meios:

-   Digitando as palavras biometria, impressão digital, face ou outras frases relacionadas na caixa de texto Iniciar pesquisa para iniciar o painel de controle de dispositivos biométricos. A lista de resultados para biometria pode conter itens como o seguinte em uma imagem do Windows 10.
    -   Configurar entrada de impressão digital
    -   Configurar entrada facial

### <a name="supported-scenarios"></a>Cenários com suporte

Os cenários a seguir têm suporte:

-   Os usuários podem fazer logon em um computador local, em um grupo de trabalho ou em um domínio usando um leitor de impressão digital ou uma câmera de IR concentrada na face.
-   Um usuário com privilégios administrativos pode elevar aplicativos por meio do UAC (controle de conta de usuário) usando uma impressão digital ou face.

## <a name="management-components"></a>Componentes de gerenciamento

Um sistema biométrico pode ser gerenciado usando Política de Grupo ou MDM (gerenciamento de dispositivo móvel).

### <a name="biometric-system-management"></a>Gerenciamento de sistema biométrico

Você pode gerenciar recursos biométricos usando Política de Grupo ou MDM. Política de Grupo pode ser usado para executar as seguintes ações:

-   Especifique o período de tempo limite para troca rápida de usuário, se implementado pelo ISV.
-   Impedir a instalação do dispositivo biométrico.
-   Forçar a remoção de drivers para dispositivos biométricos.
-   Desabilite o serviço biométrico.

 

 